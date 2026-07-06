# Async Race

**Deployed solution (frontend only):** https://mkr-sof.github.io/async__race

> ⚠️ The app talks to `http://localhost:3000`. Please clone and run the [mock server](https://github.com/mikhama/async-race-api) locally before reviewing — the deployed frontend expects it on that address.

## Score: ___ / 300
*(self-check total, excludes the 100-point "Overall Code Quality" section — reviewer-only, see below)*

---

## Getting Started

### Frontend

```bash
npm install
npm start
```

App runs at `http://localhost:5173` (Vite dev server).

### Backend (required locally)

```bash
git clone https://github.com/mikhama/async-race-api.git
cd async-race-api
npm install
npm start
```

API runs at `http://localhost:3000`.

### Running Tests

```bash
npm test
```

### Building for Production

```bash
npm run build
```

---

## ✅ Checklist ___ / 400 pts

### 🚀 UI Deployment

- [ ] **Deployment Platform:** Successfully deployed on GitHub Pages, Netlify, Vercel, Cloudflare Pages, or similar.

### ✅ Requirements to Commits and Repository

- [ ] **Commit guidelines compliance:** All commits follow Conventional Commits format (`feat:`, `fix:`, `refactor:`, `docs:`, etc.), present tense, imperative mood.
- [ ] **Checklist included in README.md**
- [ ] **Score calculation:** Checklist self-scored and total placed at the top of README.md.
- [ ] **UI Deployment link in README.md:** placed at the top, alongside the score.

### Basic Structure (80 points)

- [ ] **Two Views (10 pts):** "Garage" and "Winners".
- [ ] **Garage View Content (30 pts):**
  - [ ] Name of view
  - [ ] Car creation and editing panel
  - [ ] Race control panel
  - [ ] Garage section
- [ ] **Winners View Content (10 pts):**
  - [ ] Name of view ("Winners")
  - [ ] Winners table
  - [ ] Pagination
- [ ] **Persistent State (30 pts):** Page numbers and input states preserved when switching views.

### Garage View (90 points)

- [ ] **CRUD Operations (20 pts):** Create/update/delete cars (name + color); empty/too-long names handled; delete also removes the car from "winners".
- [ ] **Color Selection (10 pts):** RGB palette picker, shown on the car's image with its name.
- [ ] **Random Car Creation (20 pts):** Button creates 100 cars per click; name assembled from two random parts (≥10 options each); color randomized.
- [ ] **Car Management Buttons (10 pts):** Update/delete buttons near each car.
- [ ] **Pagination (10 pts):** 7 cars per page.
- [ ] **EXTRA POINTS (20 pts):**
  - [ ] Empty garage shows a friendly "No Cars" message
  - [ ] Deleting the last car on a page moves you to the previous page

### 🏆 Winners View (50 points)

- [ ] **Display Winners (15 pts):** Winning car appears in the Winners table.
- [ ] **Pagination for Winners (10 pts):** 10 winners per page.
- [ ] **Winners Table (15 pts):** Columns for №, image, name, wins, best time; repeat wins increment count and only update best time if faster.
- [ ] **Sorting Functionality (10 pts):** Sort by wins and by best time, ascending/descending, across the *entire* dataset (not just the current page).

### 🚗 Race (170 points)

- [ ] **Start Engine Animation (20 pts):** Click start → wait for velocity response → animate → drive request; stop animation on a 500 error.
- [ ] **Stop Engine Animation (20 pts):** Click stop → wait for response → car returns to start position.
- [ ] **Responsive Animation (30 pts):** Fluid down to 500px width.
- [ ] **Start Race Button (10 pts):** Races all cars on the current page.
- [ ] **Reset Race Button (15 pts):** Returns all cars to starting position.
- [ ] **Winner Announcement (5 pts):** Message shows the winning car's name.
- [ ] **Button States (20 pts):** Start disabled while driving; stop disabled at start position.
- [ ] **Actions during the race (50 pts):** Predictable behavior for delete/edit/page/view changes and new-car creation while a race is running.

### 🎨 Prettier and ESLint Configuration (10 points)

- [ ] **Prettier Setup (5 pts):** `format` and `ci:format` scripts in `package.json`.
- [ ] **ESLint Configuration (5 pts):** Airbnb config; `lint` script; strict TypeScript settings reflected.

### 🌟 Overall Code Quality (100 points) — *reviewer only, skip during self-check*

- [ ] Modular design (API / UI / state separated)
- [ ] Functions ≤ 40 lines, common logic extracted to helpers
- [ ] Minimal duplication, no magic numbers/strings
- [ ] Readable naming throughout
- [ ] Extra features (custom hooks, portals, router, etc.)

---

## Known bugs / limitations

*(Honesty here counts — a disclosed minor bug costs less than one the reviewer finds themselves.)*

-
