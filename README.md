# Code Style Policeman

**Code Style Policeman** is a real-time project command center designed for student development teams, hackathons, and collaborative software projects. It integrates version control, team communication, semantic code analysis, and AI-powered insights into a unified dashboard to monitor project health, team productivity, and knowledge distribution.

The platform connects directly with GitHub repositories to provide actionable insights, automated alerts, and intelligent project analysis.

---

## Deployment

**Application:**  
https://codestylepoliceman-theta.vercel.app/

---

## Overview

Modern development teams often struggle to track project health, identify blockers early, and understand knowledge distribution across contributors. Code Style Policeman solves this problem by combining real-time GitHub data, communication analysis, and AI insights into a single centralized dashboard.

The system automatically tracks commits, pull requests, issues, contributor activity, workflow efficiency, and communication patterns to generate a comprehensive health score and actionable recommendations.

---

## Key Features

### GitHub Integration
- OAuth-based repository access
- Automatic webhook registration
- Real-time tracking of commits, pull requests, issues, branches, and deployments
- Historical repository data synchronization
- File-level authorship tracking

### Semantic Code Analysis
- Automatic classification of commits into categories such as feature, fix, refactor, docs, test, and more
- Risk detection based on code changes
- Impact scoring based on file importance
- Commit summaries and development insights

### Project Health Monitoring
- Composite health score based on:
  - Commit velocity
  - Pull request throughput
  - Issue resolution rate
  - Contributor activity distribution
  - Team collaboration patterns
- Health trends visualization

### Flow Metrics Tracking
- Cycle time analysis
- Work-in-progress tracking per contributor
- Review and deployment time tracking
- Productivity trend monitoring

### Knowledge Distribution Analysis
- Bus factor calculation
- File ownership tracking
- Contributor knowledge graph visualization
- Risk identification from knowledge concentration

### Communication Analysis
- Message intent detection (blockers, progress updates, task claims, questions)
- Automatic blocker detection and alert generation
- Unified communication dashboard

### AI-Powered Insights
- Automated project analysis and summaries
- Task and todo generation
- Risk assessment and recommendations
- Contributor and team dynamics insights

### Alert System
Automatically detects and alerts for:
- Stale pull requests
- Inactive branches
- Blockers in communication
- High work-in-progress load
- Dependency risks
- Collaboration issues

### Workspace Management
- Multi-workspace support
- Role-based access control
- Secure invite system
- Contributor management

---

## Dashboard Modules

- Overview Dashboard
- Commits Tracking
- Pull Request Monitoring
- Issue Management
- Alert Center
- Knowledge Graph (Bus Factor)
- Team Health Analysis
- Communication Center
- AI Insights and Todo Generation
- Workspace Settings

---

## Tech Stack

### Frontend
- Next.js 15
- React 19
- TypeScript
- Tailwind CSS
- Radix UI
- shadcn/ui
- Chart.js and Recharts
- Framer Motion

### Backend
- Next.js API Routes
- Supabase (PostgreSQL)
- JWT Authentication
- GitHub OAuth
- Groq API (LLaMA 3.3 70B)

### Integrations
- GitHub Webhooks

### Testing
- Vitest
- Testing Library
- Coverage Reporting

---

## Architecture Overview

The system follows a full-stack architecture where the frontend dashboard communicates with backend API routes that process GitHub webhook events, analyze commits, run NLP on communication messages, and generate AI insights.

The backend stores structured project data in PostgreSQL and continuously updates metrics, alerts, and health scores in real time.

---

## Security

- Secure authentication using JWT
- OAuth integration with GitHub
- Webhook signature verification
- Input validation using schema validation
- Rate limiting on sensitive endpoints
- Secure token-based workspace access

---

## Use Cases

- Hackathon team monitoring
- Capstone project management
- Student development team coordination
- Collaborative software project tracking
- Engineering productivity analysis

---

## Environment Variables

Create a `.env.local` file in the root directory and configure the following variables:
```bash
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_ROLE_KEY=

GITHUB_CLIENT_ID=
GITHUB_CLIENT_SECRET=

DISCORD_CLIENT_ID=
DISCORD_CLIENT_SECRET=

JWT_SECRET=

GROQ_API_KEY=

WEBHOOK_SECRET=
```

---

## Project Structure
```bash
/app
/components
/lib
/api
/hooks
/types
/public
/tests

```
## Installation (Local Development)
```bash
git clone https://github.com/your-username/code-style-policeman.git
cd code-style-policeman
npm install
npm run dev
```

