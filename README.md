# Insurance Revision Platform — W01 Award in General Insurance

A single file, offline capable PWA for revising the W01 syllabus: ten topics, each with flashcards, quizzes, a sixty second blitz, a risk sorter, printable fact sheets and fun facts.

## Files to upload to GitHub

Upload all of these to the root of the repository (replacing the existing versions):

| File | Status |
|---|---|
| `index.html` | Updated — all new features including the vibration toggle |
| `sw.js` | Updated — cache version v7, font caching, faster loads |
| `manifest.json` | Unchanged |
| `icon.svg` | Unchanged |
| `icon-192.png` | Keep your existing copy in the repo (not included here) |
| `icon-512.png` | Keep your existing copy in the repo (not included here) |

Publishing with GitHub Pages: repository Settings, Pages, deploy from branch `main`, root folder. The service worker cache version bump makes installed apps pick up the new version automatically on their next online visit, students do not need to reinstall. Existing student progress is kept, the localStorage keys are unchanged.

## What is new in this version

Spaced repetition: cards flagged "Need to review" now come first in the deck, and a card only counts as mastered when marked "I knew it" on two different days (+5 points each time). Daily streak: a flame counter with a fourteen day calendar on the home page, practising on consecutive days builds it. Badge cabinet: twelve permanent achievements with locked and unlocked states. Mock exam: twenty questions sampled across all ten topics with a topic by topic breakdown, diagnostic only, no points. Retry missed: every quiz result offers a retry of just the questions answered wrongly. Daily Five: five quick questions drawn from each student's weakest areas across all topics. Fairer points: fact sheets award +10 only after the sheet has been open about twelve seconds, the print pack no longer awards points in bulk, and repeat quiz answers earn +2 rather than +10. Juice: true 3D card flip, confetti on perfect rounds, new bests and completed topics, optional sound effects (speaker button in the top bar, beeps on right answers) and a separate vibration toggle (📳 button, buzzes on wrong answers), both off by default, keyboard shortcuts on desktop (Space to flip, arrow keys, A to D or 1 to 4 in quizzes, K and R on flashcards, Escape for back). Sorter now shows the correct side briefly after a wrong answer. Fun facts ask for a guess before revealing (+2 points). Share score buttons on all result screens. Exam countdown: set the exam date on the home page and it shows days remaining with a suggested weekly pace. Service worker now caches Google Fonts after the first visit so the typography survives offline, and serves the shell cache first for instant loads.

## Notes

Progress, streaks and badges are stored in localStorage on the student's device, nothing is sent to a server. Reduced motion preferences are respected, animations and confetti are disabled automatically. Sound and vibration never activate without the student switching them on.
