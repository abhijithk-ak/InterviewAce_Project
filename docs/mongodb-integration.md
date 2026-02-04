# MongoDB Atlas Integration Guide

## Setup Steps

### 1. Create MongoDB Atlas Account
- Visit [MongoDB Atlas](https://www.mongodb.com/atlas)
- Create free cluster (M0 - 512MB storage)
- Whitelist your IP addresses
- Create database user

### 2. Install Dependencies
```bash
pnpm add mongodb mongoose @types/mongoose
```

### 3. Environment Variables
Add to `.env`:
```
MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.xxxxx.mongodb.net/interview-ace?retryWrites=true&w=majority
```

### 4. Database Connection
```typescript
// lib/mongodb.ts
import { MongoClient } from 'mongodb'

const uri = process.env.MONGODB_URI!
const client = new MongoClient(uri)

export async function connectDB() {
  if (!client.topology || !client.topology.isConnected()) {
    await client.connect()
  }
  return client.db('interview-ace')
}
```

## Migration Strategy

### Phase 1: Hybrid Approach (Recommended)
- Keep localStorage for immediate/temporary data
- Sync important data to MongoDB
- Implement background sync

### Phase 2: Full Migration
- Move all persistent data to MongoDB
- Use localStorage only for caching

## Storage Optimization for 500MB Limit

### Data Retention Policy
- Keep interview sessions for 6 months
- Archive older sessions to compressed format
- Limit message history per session (50 messages)

### Efficient Queries
```typescript
// Get recent sessions with projection
db.sessions.find(
  { userId: ObjectId, createdAt: { $gte: new Date(Date.now() - 30 * 24 * 60 * 60 * 1000) } },
  { messages: { $slice: -20 }, config: 1, scores: 1 }
)
```

### Indexing Strategy
```javascript
// Essential indexes only
db.sessions.createIndex({ userId: 1, createdAt: -1 })
db.notes.createIndex({ userId: 1, category: 1 })
db.users.createIndex({ githubId: 1 }, { unique: true })
```

## Estimated Storage Usage
- Users: ~1KB per user = 500 users = 500KB
- Sessions: ~10KB per session = 40,000 sessions = 400MB
- Notes: ~2KB per note = 50,000 notes = 100MB
- **Total capacity**: ~40-50K sessions with notes