# UniArchive × BuildUp UNIZIK 2026

**UniArchive** is a study-material archive for Nigerian university students: past
questions, lecture notes and textbooks, organised by university → faculty → department,
readable in the browser (even on low-end phones and offline). It's live and in use.

- Live site: https://uniarchive.com.ng
- Android app: [download the latest release](https://github.com/emmzyrayz/uniarchive-app/releases/latest)

This repository holds what we build **during BuildUp UNIZIK (2–7 November 2026)**. The
product's full source code is private; we're happy to walk judges through it live.

---

## The problem

Students pass past questions around as blurry photos and scanned PDFs in WhatsApp groups.
A scan can't be searched or practised from, so UniArchive's contributors type the
questions out by hand. With equations and options, that takes hours per paper, so
most uploaded papers are never typed.

## What we're building: a Gemini typing assistant

A **"Draft questions from this page"** button in UniArchive's typing workspace:

1. The page of the scanned paper on screen is sent to **Gemini** (vision, structured
   output).
2. Gemini returns the questions on that page: number, text (maths as LaTeX), question
   type, options and the marked answer where the paper shows one.
3. They appear as **drafts flagged "AI draft – check against the page"**. A person
   corrects and submits them, and the usual verification still applies. **The AI types;
   a human checks.**
4. Verified questions become searchable and can be used for timed practice tests.

Stretch goal, if the core is solid: an **"Explain this question"** button, generated once
per question, stored, and labelled as AI-written.

## Status

| Day | Plan |
| --- | --- |
| Before the event | Typing UNIZIK papers by hand (MAT 102, MAT 161, GST 112) and timing it as the baseline |
| 2–5 Nov | Typing assistant: page → Gemini → draft questions → review → submit |
| 5–6 Nov | Explanations (stretch), demo video |
| 7 Nov | Submission |

Code, screenshots, the demo video and the before/after typing times will be added here
during the event.

## Built with

Next.js, React, TypeScript, MongoDB, Gemini API (Google AI Studio), plus Google services
UniArchive already uses: Google sign-in, Google Drive import and Firebase Cloud Messaging.
