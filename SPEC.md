# SPEC.md — Negotiation Coach

**Developer:** Cidney Ho
**Agreed Development Fee:** 30 GIX Bucks

---

## Project Overview

A mobile-friendly web app that acts as a real-time AI negotiation coach. It listens to a live conversation via microphone and whispers short, private coaching cues to the user through their earbuds — detecting key negotiation moments like silence, pressure tactics, and concession patterns.

---

## User Stories

1. **As a student**, I want to enter context about my negotiation (role, target number, situation type) before a call, so the AI knows what to listen for.
2. **As a user**, I want the app to transcribe the conversation in real time, so it can analyze what's being said.
3. **As a user**, I want to receive short whisper-style coaching cues in my ear during the conversation, so I know what to say at the right moment.
4. **As a user**, I want the app to detect when I'm about to cave (long silence, filler words, dropping my number) and prompt me to hold firm.
5. **As a user**, I want a post-session debrief screen showing my listening ratio, number of cues fired, and one AI-written insight about my performance.
6. **As a returning user**, I want to see my past sessions so I can track how my negotiation skills improve over time.

---

## Desired Specifications

### Must-Have (MVP)
- Session setup screen — user inputs: situation type, their target number, counterpart context
- Live session screen — real-time audio transcription displayed on screen
- AI coaching cues — short whisper prompts triggered by detected negotiation signals:
  - Silence gap > 4 seconds → "Don't fill this silence — wait."
  - Trigger words ("always", "budget", "final offer") → context-aware counter prompt
  - Concession detected → "You've given ground — ask for something back."
- Post-session debrief — transcript summary, cues fired, one AI insight

### Nice-to-Have
- Session history with skill-trend chart
- Preset negotiation modes: Salary, Freelance, Rent, Car, General
- Haptic buzz on phone as alternative to audio cue

### Out of Scope (for MVP)
- Video / facial expression analysis
- Multi-user / shared sessions
- Native mobile app (iOS/Android)

---

## Tech Stack

Negotiable — open to developer's recommendation. Suggested: **Next.js + Supabase/Firebase**, Microsoft diarized speech to text  (we can get free access as student) for transcription/Whisper STT could be an option too, Gemini Flash 2.5 AI Live text to speech for coaching logic.

---

## Data Model

**`users`** — id, name, email, created_at

**`sessions`** — id, user_id, situation_type, target_number, transcript, cues_fired (JSON), debrief_insight, created_at

---

## GitHub Issues

1. Project setup — repo, env, auth, database schema
2. Session setup screen — form with situation type, target number, context
3. Live transcription — microphone input + real-time speech-to-text display
4. AI coaching engine — signal detection logic + cue generation
5. Whisper overlay UI — coaching cue display during live session
6. Post-session debrief screen — transcript summary, cues, AI insight
7. Session history view — past sessions list with basic stats
8. Polish + deployment — responsive design, final QA, deploy to Vercel
