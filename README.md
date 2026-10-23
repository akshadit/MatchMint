# 🏏 MatchMint — Sports Tournament Management & Live Scoring

[![React](https://img.shields.io/badge/React-18.2-blue?style=flat&logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.2-blue?style=flat&logo=typescript)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-5.0-646CFF?style=flat&logo=vite)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.3-38B2AC?style=flat&logo=tailwind-css)](https://tailwindcss.com/)
[![React Router](https://img.shields.io/badge/React_Router-6.22-CA4245?style=flat&logo=react-router)](https://reactrouter.com/)

> **A comprehensive tournament operations platform featuring real-time live match scoring, player registration, team owner management, and live ball-by-ball commentary.**

---

## 🌟 Overview

**MatchMint** simplifies sports tournament administration from inception to championship. Whether you are running a collegiate league, corporate cricket tournament, or local club championship, MatchMint provides a modern web interface tailored for three distinct user roles:

1. 🏃 **Players**: Self-service registration, tournament enrollment, squad confirmation, and individual career stats.
2. 🏆 **Tournament Organizers**: Bracket generation, fixture scheduling, and a designated live **Scoring Console** for real-time ball-by-ball input.
3. 💼 **Team & Franchise Owners**: Team roster management, player auction bidding, and match strategy oversight.

---

## ✨ Features

- ⚡ **Live Match Center**:
  - Dynamic scorecards displaying runs, wickets, overs, run rate, and extras.
  - Interactive ball-by-ball commentary feed with real-time updates.
  - Full squad lineups with player roles (Batsman, Bowler, All-Rounder, Wicketkeeper).
- 🎮 **Organizer Scoring Console (`/organizer/match/:id/score`)**:
  - Touch-friendly ball-by-ball input interface for scorers and umpires on-field.
  - Quick buttons for boundaries (4s, 6s), extras (wide, no-ball, bye), and dismissals.
  - Automatic strike rotation and bowler change triggers.
- 👥 **Role-Based Onboarding**:
  - Dedicated portals for Players, Organizers, and Owners.
  - Tournament selection modal with entry requirements and deadlines.
- 📰 **Activity & Media Feed**:
  - Live tournament announcements, news panels, and trending match highlights.

---

## 🗺️ Application Routing

| Route | Page | Purpose |
| :--- | :--- | :--- |
| `/` | `Home` | Featured matches, tournament highlights, activity & news |
| `/login` | `AuthPage` | User authentication |
| `/register` | `RegisterRolePage` | Role selection (Player, Organizer, Owner) |
| `/register/tournament` | `TournamentSelectPage` | Browse and enroll in active tournaments |
| `/register/player` | `PlayerRegistrationPage` | Individual player profile creation |
| `/register/organizer` | `OrganizerRegistrationPage` | Tournament organizer registration |
| `/register/owner` | `OwnerRegistrationPage` | Franchise / team owner registration |
| `/tournament/:id` | `TournamentPage` | Tournament standings, fixtures, and brackets |
| `/match/:id` | `MatchPage` | Live match scoreboard, commentary, and squad roster |
| `/organizer/match/:id/score`| `OrganizerScoringPage` | Dedicated real-time scorer interface |

---

## 🚀 Quick Start

### Prerequisites
- **Node.js** >= 18.x
- **npm** or **yarn**

### Installation
```bash
# Clone the repository
git clone https://github.com/akshadit/MatchMint.git
cd MatchMint

# Install dependencies
npm install

# Start the Vite development server
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Production Build
```bash
npm run build
npm run preview
```

---

## 🛠️ Built With

- **Vite 5**: Blazing fast frontend build tool and dev server
- **React 18**: UI component library
- **TypeScript**: Static type safety across state and match interfaces
- **Tailwind CSS**: Modern utility-first styling with responsive design
- **Lucide React**: Clean, accessible iconography
- **React Router DOM 6**: Client-side routing and deep linking

---

## 📄 License

Distributed under the MIT License.