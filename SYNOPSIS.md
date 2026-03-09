# Sonarr Calendar Tracker

A powerful, self‑hosted tool that generates a beautiful, interactive HTML dashboard of your Sonarr library and upcoming episodes. Designed for media enthusiasts who want a quick, at‑a‑glance view of their TV show collection and release schedule.

---

## Overview

The Sonarr Calendar Tracker connects to your Sonarr instance, fetches series and episode data, and produces a static HTML page that you can serve locally or embed in a dashboard. It runs periodically (via Docker) and updates the view automatically.

The generated page provides:

- A **library summary** with key statistics.
- A **calendar view** of episodes in a user‑defined date range.
- Detailed **show cards** with progress bars, episode lists, and metadata.
- **Interactive filters** to quickly find shows by title, progress, or date range status.

---

## Key Features

### 📊 Library Overview

- **Total series, downloaded episodes, missing monitored episodes** – all presented in natural language cards.
- **Series status breakdown** – continuing (including upcoming), ended.
- **Future episodes count** – total episodes scheduled beyond today.

### 📅 Calendar View

- Configurable date range (past and future days).
- Episodes grouped by show and day, with multi‑episode handling.
- Visual badges for premieres, finales, and specials.

### 🎴 Show Cards

Each card displays:

- Poster image (with fanart/poster quality options).
- Show metadata (year, network, runtime, rating, genres).
- **Three progress bars**:
  - Overall series progress.
  - Progress for episodes in the selected date range.
  - Current season progress.
- Colour‑coded dot indicating date‑range progress.
- Expandable list of episodes in the date range.

### 🔍 Interactive Filters

- **Search** by show title.
- **Progress filters** based on:
  - Season completion.
  - Current season progress (High / Medium / Low).
  - Date range progress (≥75% / <25%).
  - Shows that have episodes in the current range.
- **Jump to show** dropdown for quick navigation.
- **Clear filters** button to reset everything.

### 🎨 Themes & Visuals

- Dark / Light theme toggle (persisted in local storage).
- Consistent colour coding for progress levels (complete → green, not started → red).
- Hover effects and smooth animations.

### 🚀 Performance & Maintainability

- Static HTML – fast to load, no server‑side rendering after generation.
- Image caching to reduce Sonarr API load.
- Modular Python code with clear separation of concerns (API client, data models, HTML generator).
- Extensive Jinja2 template with reusable macros and CSS classes.

---

## Installation

### Docker (Recommended)

A `docker-compose.yml` is provided. Set the required environment variables and run:

```bash
docker-compose up -d
```
