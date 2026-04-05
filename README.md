# MacroTrack Pro 🏋️

**A full-stack AI-powered fitness and nutrition tracking web app — built for serious athletes.**

🔗 **[Live Demo](https://brahmalabsai-arch.github.io/macrotrack-pro/)** ← *(replace with your actual URL)*

---

## What It Does

MacroTrack Pro is a mobile-first progressive web app that helps you track your macros, log workouts, and get AI-powered nutrition and fitness guidance — all in one place.

### Core Features

- **Smart Macro Tracking** — Log meals across breakfast, lunch, dinner and snacks. Tracks calories, protein, carbs and fats against personalised daily targets calculated from your BMR/TDEE.
- **AI Food Search** — Three-mode food lookup: a quick database of 100+ Indian and global foods, an Open Food Facts search (millions of items, no API key needed), and a photo scan mode powered by Claude Vision.
- **📷 Meal Photo Scanning** — Take or upload a photo of your meal. AI identifies every food item, estimates portion sizes, and returns macro breakdowns — tap to log instantly.
- **Workout Logger** — 80+ exercises across 12 muscle groups (Chest, Back, Shoulders, Biceps, Triceps, Legs, Glutes, Calves, Core, Forearms, Cardio, Full Body). Logs sets × reps with calorie burn estimates.
- **AI Coach** — Built-in chat assistant with two modes: Recipe Generator (describe your ingredients → get a healthy recipe) and Fitness Q&A (evidence-based answers on nutrition, workouts, and health).
- **Progress Tracking** — 7-day weight trend chart with smart coaching tips based on your goal pace.
- **User Accounts & Cloud Sync** — Full Firebase Authentication (register/login) and Firestore database. Your data persists across sessions and devices.
- **Day Commit System** — Lock a day's logs to prevent accidental edits. Only committed data counts toward weekly progress.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 18 (via Babel, no build step) |
| Database | Firebase Firestore |
| Auth | Firebase Authentication |
| AI / Vision | Anthropic Claude API (claude-haiku) |
| Food Data | Open Food Facts API |
| CORS Proxy | Cloudflare Workers |
| Hosting | GitHub Pages |

---

## Screenshots

*Coming soon*

---

## How to Run Locally

This is a single-file HTML app — no install, no build step, no dependencies.

1. Download `index.html`
2. Open it in any modern browser
3. Register an account and start tracking

For AI features (Photo Scan, Recipe Generator, Fitness Q&A), you will need an [Anthropic API key](https://console.anthropic.com). The app includes a step-by-step guide to get one.

---

## Project Background

This project was built entirely through **AI-assisted development using [Claude](https://claude.ai)** by Anthropic — a workflow commonly known as vibe coding.

Every feature — from the Firebase integration and Cloudflare Worker proxy, to the AI food recognition and the warm mellow UI redesign — was specified, reviewed, debugged, and iterated on through conversation with Claude. No external frameworks, no boilerplate templates, no pre-existing codebase.

This represents a new paradigm in software development: the ability to go from idea to fully functional, production-ready application through directed AI collaboration. The result is a real app with real users, real cloud infrastructure, and real AI integrations — built without traditional coding overhead.

---

## Architecture Notes

- **Single HTML file** — entire app including React components, Firebase SDK, food database, and exercise library lives in one file. Intentional choice for simplicity and portability.
- **Cloudflare Worker** acts as a CORS proxy between the browser and Anthropic's API, since browsers block direct API calls from local/static origins.
- **Firestore data model** — each user gets a document at `users/{uid}` with profile/targets, and a subcollection document at `users/{uid}/data/daily` storing all daily logs as a date-keyed map.

---

## Roadmap

- [ ] Google Sign-In support
- [ ] PWA / installable on mobile home screen  
- [ ] Weekly email summary
- [ ] Barcode scanner for packaged foods
- [ ] Custom food entries saved to user profile
- [ ] Dark mode toggle

---

## License

MIT — free to use, modify, and distribute.

---

*Built with Claude · Deployed on GitHub Pages · Data stored on Firebase*
