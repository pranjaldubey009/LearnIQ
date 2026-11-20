LearnIQ | AI-Powered Technical Interview Simulator
<p align="center">
  <strong>Practice interviews built around the code you actually write.</strong><br/>
  Turn GitHub projects and your resume into personalized technical interview sessions.
</p><p align="center">
  <a href="https://learniq-abhi.vercel.app/">Live Demo</a> ·
  <a href="https://github.com/pranjaldubey009/LearnIQ">Repository</a>
</p><p align="center">
  <img src="https://img.shields.io/badge/AI-Gemini-orange?style=flat-square" alt="Gemini AI"/>
  <img src="https://img.shields.io/badge/Frontend-React%20%7C%20TypeScript-3178C6?style=flat-square" alt="React TypeScript"/>
  <img src="https://img.shields.io/badge/Runtime-Bun-black?style=flat-square" alt="Bun"/>
  <img src="https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=flat-square" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/ORM-Prisma-2D3748?style=flat-square" alt="Prisma"/>
</p>✦ What is LearnIQ?
LearnIQ is an AI-assisted technical interview practice platform that uses a developer's GitHub profile, repository context and optional resume to create a more personalized mock interview experience.

Rather than relying only on generic question banks, LearnIQ aims to make interview practice relevant to the projects and technologies a developer has worked with—helping them prepare to explain implementation choices, code, architecture and trade-offs.
Core idea: Your projects become your interview practice material.

✦ Product Preview
Landing Page

Interview Experience

Features

✦ Architecture

<details>
<summary>Text-based architecture flow</summary>```mermaid
flowchart TD
    U[Developer] --> FE[React + TypeScript Frontend]
    FE --> API[Bun Backend API]
    FE <--> VO[Browser Voice Interface]
    VO --> API
    API --> GH[GitHub API / Repository Context]
    API --> AI[Google Gemini]
    API --> ORM[Prisma ORM]
    ORM --> DB[(PostgreSQL)]
    GH --> CTX[Technical Context]
    AI --> Q[Question Generation / Feedback]
```
</details>✦ Experience Flow
Stage	What happens
01 · Profile	Enter a GitHub username or profile URL.
02 · Analysis	Gather relevant public profile and repository context.
03 · Resume	Optionally upload a PDF or TXT resume for additional context.
04 · Preparation	Generate interview questions tailored to the available technical context.
05 · Interview	Practice through the supported interactive interview flow.
06 · Feedback	Review AI-generated evaluation and improvement suggestions.


✦ Highlights
- Repository-aware preparation — practice around your projects and technologies.
- GitHub profile context — use public profile and repository information as input.
- Resume-aware workflow — optional PDF/TXT resume context.
- AI-generated questions — personalized prompts based on available information.
- Interactive interview flow — voice-oriented functionality where supported by the implementation and browser.
- Feedback loop — AI-generated evaluation and suggestions to guide further practice.
✦ Technology
Layer	Technology	Role
Frontend	React, TypeScript	Interface and client-side experience
Runtime / tooling	Bun	Runtime and project tooling
AI	Google Gemini	AI analysis, generation and feedback
Repository context	GitHub API	Public profile and repository data
Database	PostgreSQL	Persistent application data
ORM	Prisma	Database access
Deployment	Vercel	Frontend hosting
Monorepo tooling	Turborepo	Workspace orchestration


✦ Repository Layout
LearnIQ/
├── apps/
│   ├── frontend/
│   └── backend/
├── packages/
├── docs/
│   └── images/
│       ├── landing-page.png
│       ├── interview-dashboard.png
│       ├── features.png
│       └── architecture.png
├── package.json
├── turbo.json
└── README.md
Directory names may differ from this illustrative layout as the codebase evolves.

✦ Run Locally
Prerequisites
- Bun
- Git
- PostgreSQL
- Google Gemini API key
1. Clone
git clone https://github.com/pranjaldubey009/LearnIQ.git
cd LearnIQ
2. Install dependencies
bun install
3. Configure environment
Create the backend .env file and provide your own values:
DATABASE_URL=your_postgresql_connection_string
GEMINI_API_KEY=your_gemini_api_key
GITHUB_TOKEN=your_github_token_optional
Never commit credentials or secrets.
4. Prepare the database
Run the Prisma command from the workspace where the backend Prisma configuration is available:
bunx prisma db push
5. Start development
bun run dev
Follow the local URL printed by the development process.
✦ Deployment Notes
The frontend demo is hosted on Vercel. A fully functioning production deployment also needs the backend service, database, environment variables and frontend-to-backend configuration deployed and configured correctly.
✦ Responsible Use & Limitations
- GitHub analysis is limited by the data available through public repositories and configured API access.
- AI-generated questions, summaries and evaluations can contain inaccuracies; use them as practice guidance, not authoritative hiring decisions.
- Voice functionality depends on browser support and the features implemented in the application.
- Do not upload sensitive personal information or confidential code unless you understand how it is processed and have permission to share it.
✦ Roadmap
- [ ] Deeper code and architecture analysis
- [ ] More interview difficulty and role options
- [ ] Interview history and progress tracking
- [ ] Expanded evaluation and feedback insights
- [ ] Additional language and framework coverage
- [ ] Further improvements to voice interaction
✦ Origin & Acknowledgements
LearnIQ is an adaptation and further development inspired by SkillWiseAI.

Original inspiration: https://github.com/vartika6451/SkillWiseAI

This README acknowledges the inspiration and does not imply ownership of third-party code or grant rights beyond the applicable original licenses and permissions.
✦ Developer
Abhiman Dubey
GitHub Profile
✦ License
This repository includes an MIT License file for LearnIQ as distributed in this repository. Third-party or previously existing code remains subject to its original licensing terms and any required permissions.
<p align="center">
  <strong>Build confidence by practicing with your own projects.</strong><br/>
  LearnIQ
</p>
