# Student Companion

A mobile-first study helper for BSEB Bihar Board students in Classes 10–12. Built as a static web app so it can be deployed without a build step.

## Features

- Study planner with Today, 1 week, 10 days, 2 weeks, 1 month, and custom 1–60 day ranges.
- Add, complete, and delete study tasks.
- Create practice quizzes from selectable text in chapter PDFs (5–30 questions).
- Draft flashcards from PDF text and save selected cards.
- Local progress tracking and installable PWA app shell.
- Responsive interface for mobile and desktop.

## Deploy to Vercel

1. Open [Vercel](https://vercel.com/) and choose **Add New → Project**.
2. Import `raviraj437700-cyber/Student-Companion` from GitHub.
3. Keep the framework preset as **Other** and leave Build Command and Output Directory empty/default.
4. Deploy. The app entry point is `index.html`.

## Important limitations

- This version uses browser-side text extraction and simple heuristics; quiz questions and flashcards are drafts, not AI-verified study material or official BSEB questions.
- Scanned/image-only PDFs need OCR, which is not included.
- PDF text extraction requires internet access to load PDF.js the first time.
- Tasks, saved cards, and quiz history are stored in the current browser on the current device; they do not sync across devices.
- The app shell can open offline after it has been cached, but PDF processing still needs the PDF.js library to be available.

## Files

- `index.html` — application UI and logic
- `manifest.json` — installable web app metadata
- `sw.js` — service worker for app-shell caching
- `icon.svg` — app icon

The app is kept in this repository separately; no other repository is changed by these updates.
