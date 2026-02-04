<div align="center">

<!-- Logo -->
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' rx='28' fill='%23ffffff'/%3E%3Ctext x='60' y='88' text-anchor='middle' font-family='system-ui, -apple-system, BlinkMacSystemFont, sans-serif' font-size='80' font-weight='700' fill='%23000000'%3EI%3C/text%3E%3C/svg%3E"/>
  <source media="(prefers-color-scheme: light)" srcset="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' rx='28' fill='%23000000'/%3E%3Ctext x='60' y='88' text-anchor='middle' font-family='system-ui, -apple-system, BlinkMacSystemFont, sans-serif' font-size='80' font-weight='700' fill='%23ffffff'%3EI%3C/text%3E%3C/svg%3E"/>
  <img alt="InterviewAce Logo" src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Crect width='120' height='120' rx='28' fill='%23000000'/%3E%3Ctext x='60' y='88' text-anchor='middle' font-family='system-ui, -apple-system, BlinkMacSystemFont, sans-serif' font-size='80' font-weight='700' fill='%23ffffff'%3EI%3C/text%3E%3C/svg%3E" width="120"/>
</picture>

# InterviewAce

### Master Your Technical Interviews with AI

[![Next.js](https://img.shields.io/badge/Next.js-16.0-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-4.0-38bdf8?style=flat-square&logo=tailwindcss)](https://tailwindcss.com/)
[![OpenRouter](https://img.shields.io/badge/Powered%20by-OpenRouter-6366f1?style=flat-square)](https://openrouter.ai/)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

<p align="center">
  <strong>AI-powered mock interviews • Real-time feedback • Personalized coaching</strong>
</p>

[**Get Started**](#-quick-start) · [**Features**](#-features) · [**Demo**](#-demo) · [**Documentation**](#-documentation)

---

</div>

## ✨ Features

<table>
<tr>
<td width="33%" align="center">

### 🤖 AI Interview Coach

Real-time voice and code analysis with instant feedback on your responses

</td>
<td width="33%" align="center">

### 💻 Live Coding Environment

Interactive coding environment supporting 30+ programming languages

</td>
<td width="33%" align="center">

### 📊 Smart Analytics

Track your progress, identify knowledge gaps, and measure improvement over time

</td>
</tr>
<tr>
<td width="33%" align="center">

### 🎯 Multiple Interview Types

Technical, Behavioral, System Design, and HR Screen practice sessions

</td>
<td width="33%" align="center">

### 🌓 Dark & Light Mode

Beautiful, accessible interface with theme switching support

</td>
<td width="33%" align="center">

### 📲 PWA Support

Install as a native app on any device for seamless practice anywhere

</td>
</tr>
</table>

## 🚀 Quick Start

### Prerequisites

- **Node.js** 18.0 or higher
- **pnpm** (recommended) or npm
- **GitHub Account** for authentication
- **OpenRouter API Key** for AI features

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/interview-ace.git
cd interview-ace

# Install dependencies
pnpm install

# Set up environment variables
cp .env.example .env
```

### Environment Configuration

Create a `.env` file with the following variables:

```env
# Authentication
AUTH_SECRET="your-secret-key"
AUTH_GITHUB_ID="your-github-oauth-id"
AUTH_GITHUB_SECRET="your-github-oauth-secret"

# OpenRouter AI
OPENROUTER_API_KEY="your-openrouter-api-key"
OPENROUTER_MODEL="google/gemini-2.0-flash-exp:free"

# App URL
NEXTAUTH_URL="http://localhost:3000"
```

### Development

```bash
# Start the development server
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Production Build

```bash
# Build for production
pnpm build

# Start production server
pnpm start
```

## 🎬 Demo

<div align="center">

| Dashboard | Interview Session |
|:---------:|:-----------------:|
| Overview of your progress and upcoming sessions | Real-time AI-powered mock interview |

| Analytics | Settings |
|:---------:|:--------:|
| Detailed performance insights | Customize your experience |

</div>

## 📁 Project Structure

```
interview-ace/
├── app/                    # Next.js App Router
│   ├── (app)/             # Authenticated routes
│   │   ├── dashboard/     # Main dashboard
│   │   ├── interview/     # Interview sessions
│   │   ├── analytics/     # Performance analytics
│   │   ├── questions/     # Question bank
│   │   ├── notes/         # Interview notes
│   │   ├── review/        # Session review
│   │   └── settings/      # User settings
│   ├── (marketing)/       # Public landing page
│   └── api/               # API routes
│       └── chat/          # AI chat endpoint
├── components/            # Reusable components
│   ├── ui/               # Base UI components
│   ├── ui-custom/        # Custom styled components
│   ├── views/            # Page-level components
│   └── providers/        # Context providers
├── lib/                   # Utilities and helpers
├── hooks/                 # Custom React hooks
├── public/               # Static assets
└── styles/               # Global styles
```

## 🛠️ Tech Stack

| Category | Technologies |
|----------|-------------|
| **Framework** | Next.js 16, React 19, TypeScript |
| **Styling** | Tailwind CSS 4, Framer Motion |
| **AI/ML** | OpenRouter, Vercel AI SDK |
| **Auth** | NextAuth.js (GitHub OAuth) |
| **UI Components** | Radix UI, Lucide Icons |
| **Form Handling** | React Hook Form, Zod |
| **Charts** | Recharts |

## 📖 Documentation

### Interview Types

| Type | Description |
|------|-------------|
| **Technical** | Data structures, algorithms, and coding challenges |
| **Behavioral** | STAR method questions about past experiences |
| **System Design** | Architecture and scalability discussions |
| **HR Screen** | Cultural fit and career goals assessment |

### AI Feedback System

After each response, you receive detailed feedback:

- **Technical Accuracy** (40 pts) — Correctness of your answer
- **Communication Clarity** (30 pts) — How well you explained your thoughts
- **Confidence & Delivery** (20 pts) — Presentation and poise
- **Relevance & Structure** (10 pts) — Organization of your response

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **[OpenRouter](https://openrouter.ai/)** — AI model routing and access
- **[Vercel](https://vercel.com/)** — Hosting and deployment
- **[Radix UI](https://radix-ui.com/)** — Accessible component primitives

---

<div align="center">

**[⬆ Back to Top](#interviewace)**

<sub>Built with ❤️ for developers preparing for their dream jobs</sub>

</div>
