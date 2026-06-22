# 🚀 InfraWatch AI – Multi-LLM DevOps Copilot

<div align="center">

<img src="https://placehold.co/1200x300/1e293b/ffffff?text=InfraWatch+AI+-+DevOps+Copilot" alt="InfraWatch AI Banner"/>

### AI-Powered Infrastructure Monitoring, Incident Analysis & Multi-LLM Platform

Monitor infrastructure, analyze logs with Gemini AI, receive intelligent alerts, and compare responses across multiple LLMs from a single platform.

Built with **Next.js, Clerk, Supabase, Docker, Redis, Nginx, Python, Gemini API, and GitHub Actions.**

</div>

---

## 📌 Overview

InfraWatch AI started as a Multi-LLM Chat System and evolved into a complete DevOps + AIOps platform.

The system enables users to:

* Compare responses from multiple LLMs simultaneously
* Persist chat history securely
* Monitor infrastructure health
* Analyze logs using AI
* Detect incidents automatically
* Receive email alerts
* Track API usage and system metrics
* Manage deployments using DevOps best practices

---

# 🏗 Architecture

```text
User
 │
 ▼
Clerk Authentication
 │
 ▼
Nginx Reverse Proxy
 │
 ▼
Next.js Application
 │
 ├────────► Gemini API
 │
 ├────────► OpenAI API
 │
 ├────────► Claude API
 │
 ├────────► Supabase PostgreSQL
 │
 └────────► Redis Cache
                 │
                 ▼
          Monitoring Service
                 │
                 ▼
            Gmail Alerts
                 │
                 ▼
         AI Log Analyzer
                 │
                 ▼
        Incident Dashboard
```

---

# ✨ Core Features

## 🤖 Multi-LLM Chat System

* GPT Support
* Gemini Support
* Claude Support
* Side-by-side response comparison
* Streaming responses
* Custom temperature settings
* Model selection panel

---

## 🔐 Authentication

Powered by Clerk.

Features:

* Google Login
* GitHub Login
* Secure Session Management
* Protected Dashboard Routes

---

## 💬 Persistent Chat History

Stored in Supabase PostgreSQL.

Features:

* Conversation storage
* Message history
* Search conversations
* Continue previous chats

---

## 📊 Usage Analytics

Track:

* Total Requests
* Token Consumption
* Model Usage
* Response Statistics

---

## ⚡ Redis Caching

Features:

* Gemini response caching
* Faster repeated queries
* Reduced API costs
* Session optimization

---

## 🐳 Dockerized Infrastructure

Application runs in isolated containers.

Services:

* Next.js
* Redis
* Monitoring Service
* Nginx

Benefits:

* Reproducible environments
* Easy deployment
* Simplified scaling

---

## 🔄 CI/CD Pipeline

GitHub Actions automatically:

* Install dependencies
* Run lint checks
* Run type checking
* Build application
* Build Docker image
* Validate deployment readiness

---

## 📈 Infrastructure Monitoring

Python monitoring service tracks:

* CPU Usage
* Memory Usage
* Disk Usage
* Container Health
* Service Availability

Metrics are stored in Supabase and displayed in real time.

---

## 🧠 AI Log Analysis

Powered by Gemini API.

The system automatically analyzes:

* Application Logs
* Nginx Logs
* Docker Logs
* Infrastructure Errors

Generates:

* Root Cause Analysis
* Severity Classification
* Suggested Fixes
* Confidence Score

Example:

```json
{
  "root_cause": "Redis Container Unavailable",
  "severity": "High",
  "suggested_fix": "Restart Redis Container",
  "confidence": 91
}
```

---

## 📧 Smart Email Alerts

Automatic Gmail notifications for:

* High CPU Usage
* High Memory Usage
* Disk Space Issues
* Container Failures
* Critical Incidents

Example:

```text
🚨 InfraWatch Alert

Service:
Redis

Issue:
Container Down

Suggested Action:
Restart Service

Severity:
High
```

---

## 📊 DevOps Dashboard

Route:

```text
/admin/devops
```

Features:

* Live CPU Metrics
* RAM Usage
* Disk Usage
* Container Status
* Alert History
* AI Incidents
* Gemini Usage Statistics
* Redis Cache Metrics

---

## 📱 Progressive Web App (PWA)

Features:

* Installable
* Responsive
* Offline Support
* Mobile Friendly

---

# 🛠 Tech Stack

## Frontend

* Next.js 15
* React
* TypeScript
* Tailwind CSS
* Zustand

## Authentication

* Clerk

## Database

* Supabase PostgreSQL

## Caching

* Redis

## DevOps

* Docker
* Docker Compose
* Nginx
* GitHub Actions

## Monitoring

* Python
* psutil

## AI

* Gemini API
* OpenAI API
* Claude API

## Deployment

* WSL Ubuntu
* Docker

---

# 📂 Project Structure

```text
infra-watch-ai/

├── app/
├── components/
├── lib/
│
├── services/
│   ├── monitoring/
│   │   ├── cpu.py
│   │   ├── memory.py
│   │   ├── disk.py
│   │   └── alerts.py
│   │
│   └── ai-analysis/
│       └── analyze_logs.py
│
├── docker/
│   ├── Dockerfile
│   └── nginx.conf
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── supabase/
│   └── migrations/
│
└── README.md
```

---

# ⚙️ Installation

## Prerequisites

* Node.js 22+
* Docker Desktop
* WSL Ubuntu
* Redis
* Supabase Project
* Clerk Account
* Gemini API Key

---

## Clone Repository

```bash
git clone https://github.com/Darshan3690/Multi-LLM-Chat-System.git

cd Multi-LLM-Chat-System
```

---

## Install Dependencies

```bash
npm install
```

---

## Environment Variables

Create `.env.local`

```env
# Clerk
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=

# Supabase
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_KEY=

# Gemini
GEMINI_API_KEY=

# Redis
REDIS_URL=redis://localhost:6379

# Gmail
GMAIL_USER=
GMAIL_APP_PASSWORD=
ALERT_EMAIL=

# App
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

---

# 🐳 Run With Docker

Build:

```bash
docker compose build
```

Start:

```bash
docker compose up
```

Stop:

```bash
docker compose down
```

---

# 💻 Local Development

```bash
npm run dev
```

Open:

```text
http://localhost:3000
```

---

# 🔄 CI/CD Workflow

```text
Push Code
     │
     ▼
GitHub Actions
     │
     ▼
Lint
     │
     ▼
Type Check
     │
     ▼
Build
     │
     ▼
Docker Build
     │
     ▼
Deployment Ready
```

---

# 📸 Screenshots

Add:

* Multi-LLM Chat UI
* DevOps Dashboard
* AI Incident Analysis
* Monitoring Dashboard
* Gmail Alerts

---

# 🚀 Future Enhancements

* Kubernetes Deployment
* Grafana Dashboard
* Prometheus Integration
* Slack Notifications
* AWS Deployment
* AI Auto-Remediation
* Multi-Server Monitoring
* Incident Prediction

---

# 🤝 Contributing

Contributions are welcome.

1. Fork Repository
2. Create Feature Branch

```bash
git checkout -b feature/amazing-feature
```

3. Commit Changes

```bash
git commit -m "Add amazing feature"
```

4. Push

```bash
git push origin feature/amazing-feature
```

5. Create Pull Request

---

# 📄 License

Distributed under the MIT License.

---

<div align="center">

Made with ❤️ by Darshan Rajput

Building the future of AI-powered DevOps 🚀

</div>
