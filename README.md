# 🎯 Negotiation Coach

> Your AI coach that whispers what to say — live, in your ear.

Negotiation Coach is a real-time AI-powered web app that listens to your negotiation conversations and privately coaches you through your earbuds. It detects key moments — silence, pressure tactics, trigger words — and whispers the right move before you cave.

Built for students, freelancers, and anyone who knows what they should say but freezes when it matters.

---

## The Problem

Most people lose negotiations not because they lack knowledge, but because pressure kills execution in the moment. There's no tool that coaches you *live*, while the conversation is happening.

**Example:** A student on a call with a recruiter offering $22/hr knows the market rate is $28 — but the moment the recruiter says "this is what we offer all interns," they freeze and accept. One whispered sentence could have earned them $800 more over the summer.

---

## Key Features

- **Session setup** — input your situation, target number, and context before the call
- **Live transcription** — real-time speech-to-text displayed on screen
- **AI whisper cues** — short coaching prompts triggered by detected negotiation signals
- **Post-session debrief** — transcript summary, cues fired, and one AI insight
- **Session history** — track your improvement over time

---

## Developer

**Cidney Ho**
Agreed fee: 30 GIX Bucks

---

## Timeline & Check-in Points

| # | Milestone | Due Date | Required Progress |
|---|---|---|---|
| 1 | **Architecture check-in** | Week 1 | Repo setup, database schema, auth working, initial PR submitted |
| 2 | **Core feature check-in** | Week 2 | Live transcription working + at least 2 coaching cues firing correctly |
| 3 | **Full flow check-in** | Week 3 | Setup → Live session → Debrief flow fully functional end-to-end |
| 4 | **Final delivery** | Week 4 | All MVP features complete, deployed to Vercel, session history working |

> Client will review and respond to all Pull Requests within 48 hours.

---

## Tech Stack

- Frontend: Next.js
- Backend/DB: Firebase/Supabase
- Transcription: Microsoft Speech to Text (Diarized) 
- AI Coaching: Gemini Flash 2.5
- Deployment: Vercel

---

## Getting Started

```bash
git clone <repo-url>
cd negotiation-coach
npm install
cp .env.example .env.local
npm run dev
```
