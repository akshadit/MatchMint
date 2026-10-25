# 🏏 MatchMint — Sports Tournament Management & Live Scoring Platform

[![React](https://img.shields.io/badge/React-18.2-blue?style=for-the-badge&logo=react&logoColor=white)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.2-blue?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-5.0-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.3-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![React Router](https://img.shields.io/badge/React_Router-6.22-CA4245?style=for-the-badge&logo=react-router&logoColor=white)](https://reactrouter.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

> **A comprehensive sports tournament operations platform featuring real-time live ball-by-ball scoring, interactive player auction & bidding rooms, automated fixtures, points standings, and role-based portals.**

---

## 🌟 Overview

Organizing grassroots, collegiate, and corporate sports tournaments is notoriously fragmented—scattered between paper scorebooks, WhatsApp groups, spreadsheets, and manual bracket calculations.

**MatchMint** unifies the entire tournament lifecycle into a slick, responsive web platform tailored for three distinct participant personas:

1. 🏆 **Tournament Organizers**: Bracket generation, fixture scheduling, squad roster management, and a dedicated **On-Field Live Scoring Console** (`/organizer/match/:id/score`).
2. 💼 **Franchise & Team Owners**: Real-time **Player Auction & Bidding Room**, virtual purse management, team roster curation, and performance analytics.
3. 🏃 **Players & Athletes**: Self-service registration, tournament enrollment, squad verification, individual strike rates, bowling averages, and career leaderboards.

---

## ✨ Key Feature Suites

### 1. ⚡ Live Match Center (`/match/:id`)
- **Dynamic Live Scoreboard**: Real-time updates for total runs, wickets fallen, overs completed, current run rate (CRR), and required run rate (RRR).
- **Interactive Ball-by-Ball Feed**: Chronological commentary stream showing boundaries (4s, 6s), extras, wicket dismissals, and bowling milestones.
- **Full Squad Scorecards**: Detailed breakdown of Batsmen (Runs, Balls, 4s, 6s, Strike Rate) and Bowlers (Overs, Maidens, Runs, Wickets, Economy).
- **Head-to-Head Squad Rosters**: Verified playing XI and bench lineups.

### 2. 🎮 Organizer Scoring Console (`/organizer/match/:id/score`)
- **Touch-Optimized Umpire HUD**: Designed for instantaneous touch input on mobile devices directly beside the pitch.
- **Fast Action Buttons**: Quick-tap scoring for `0`, `1`, `2`, `3`, `4`, `6`, and extras (`Wide`, `No Ball`, `Leg Bye`, `Bye`, `Penalty`).
- **Dismissal Modals**: Bowled, Caught, LBW, Run Out, Stumped, Hit Wicket.
- **Automated Over & Strike Rotation**: Automatically rotates batting strike at over completion or odd-run singles.

### 3. 🔨 Live Player Auction & Bidding Room
- **Interactive Bidding Console** (`TournamentAuction.tsx`): Real-time bidding system for team owners during draft day.
- **Purse & Budget Tracking**: Monitors team purse balance, remaining player slots, and minimum base bid increments.
- **Player Draft Catalog**: Filter prospective players by specialization (Batsman, Pace Bowler, Spin Bowler, All-Rounder, Wicketkeeper).

### 4. 📊 Tournament Standings & League Tables
- **Automated Points Table** (`TournamentTable.tsx`): Tracks Matches Played (P), Won (W), Lost (L), Tied (T), Net Run Rate (NRR), and Total Points (Pts).
- **Fixtures & Scheduling Matrix** (`TournamentFixtures.tsx`): Upcoming matchups, match venues, toss results, and match outcome badges.
- **Player & Team Stats Widgets** (`PlayerStatsWidgets.tsx`, `TeamStatsWidgets.tsx`): Visual performance cards for tournament top scorers (Orange Cap) and leading wicket-takers (Purple Cap).

---

## 🗺️ Application Routing Architecture

```
/
├── /login                            # Unified authentication portal
├── /register                         # Role selection (Player / Organizer / Owner)
│   ├── /register/tournament          # Browse and register in active tournaments
│   ├── /register/player              # Athlete profile creation
│   ├── /register/organizer           # Organizer credentials registration
│   └── /register/owner               # Franchise owner onboarding
├── /tournament/:id                   # Tournament hub (Fixtures, Table, Teams, Auction)
├── /match/:id                        # Live match scoreboard, commentary, lineups
└── /organizer/match/:id/score        # Dedicated umpire/scorer ball-by-ball console
```

---

## 🏗️ Project Structure

```
MatchMint/
├── public/
│   └── bg.png                       # High-res sports stadium background
├── src/
│   ├── App.tsx                      # Root route declarations & router setup
│   ├── main.tsx                     # React 18 DOM mount point
│   ├── index.css                    # Tailwind CSS configuration & design tokens
│   ├── context/
│   │   └── AuthContext.tsx          # Role-based user session provider
│   ├── data/
│   │   └── mockData.ts              # Preset tournament, team, and match data
│   ├── components/
│   │   ├── auth/                    # Modal registration & tournament select dialogs
│   │   ├── home/                    # Activity feed, featured matches, news updates
│   │   ├── layout/                  # Navigation bar and responsive sidebar
│   │   ├── match/                   # Scoreboard, Commentary, Scorecard, Squads
│   │   └── tournament/              # Auction room, Fixtures, Points table, Stats
│   └── pages/                       # Screen views corresponding to routes
├── tailwind.config.js
├── tsconfig.json
└── vite.config.ts
```

---

## 🚀 Getting Started

### Prerequisites
- **Node.js** >= 18.x
- **npm** or **yarn** / **pnpm**

### Installation
```bash
# 1. Clone the repository
git clone https://github.com/akshadit/MatchMint.git
cd MatchMint

# 2. Install dependencies
npm install

# 3. Start local development server
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Production Build
```bash
# Compile TypeScript and bundle with Vite
npm run build

# Preview production build locally
npm run preview
```

---

## 📄 License

Distributed under the [MIT License](LICENSE).
