# MedQ Pro — starter project

An early responsive frontend starter for a free USMLE Step 1 question bank. This is **not yet a deployed website** and does not yet connect authentication, persistence, or the Supabase database. The included UI uses sample questions and client-side state.


## Included
- Next.js App Router + TypeScript
- Responsive dashboard and practice-question layout
- Sample original educational questions (review clinically before publishing)
- Answer feedback, distractor explanations, bookmark and incorrect-review UI (in-memory only)
- Ad placeholder on the Dashboard only; no pop-ups, no forced ads, no ad interruptions inside questions
- Supabase SQL starter schema for profiles, questions, attempts, bookmarks, and basic row-level security


## Run locally
1. Install Node.js LTS (18.18+ recommended for Next 15; 20 LTS is a safe choice).
2. Extract this folder and open it in a terminal.
3. Run `npm install`
4. Run `npm run dev`
5. Open the local address printed by Next.js (usually http://localhost:3000).


## Next backend setup
1. Create a Supabase project.
2. Open the SQL Editor and run `supabase/schema.sql`.
3. Copy `.env.example` to `.env.local` and add your Supabase project URL and anon key.
4. Implement auth and wire question, bookmark, and attempt queries. The current frontend does not use Supabase yet.
5. Before production, review the RLS policies with a security professional. In particular, do not allow students to update their own `role`; the sample profile policy should be tightened to prevent privilege escalation (e.g. separate profile fields or a trigger).


## Deploy
Deploy the Next.js app to a hosting provider such as Vercel after connecting a Git repository. Configure environment variables in the hosting dashboard. This package has not been deployed or tested against a live Supabase project.


## Content note
Sample questions are written as starter educational content. They are not a substitute for professional medical education review. Verify every question, explanation, and reference before publishing.
