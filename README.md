# Smart Digital Media Hub Pro (Serverless Static Edition)

A self-contained, enterprise-grade, glassmorphic digital media streaming and curation dashboard. It aggregates Movies (TMDB API), Music (Spotify API), Books (Google Books API), and Podcasts (iTunes Search API), running entirely serverless inside the user's browser client using `localStorage`.

---

## Architecture & Tech Stack

### Static Monorepo Layout
*   **`/frontend`**: React + Vite, Axios, Framer Motion, Context API session stores, and Recharts metrics dashboard.
*   **Browser Database**:
    *   `mediahub_users`: Manages registered accounts (pre-seeded with standard test user and admin sessions).
    *   `mediahub_interactions`: Tracks watchlist queues, liked favorites, and playing history states.
    *   `mediahub_reviews`: Community review comments.
    *   `mediahub_notifications`: Broadcast alerts.

### APIs & Fallbacks
To make this project work immediately out-of-the-box without keys, it operates on a hybrid service model. If Spotify/TMDB key variables are left blank in `.env`, the system automatically falls back to a massive mock content catalog containing royalty-free music and podcast files that actually play in the player!

---

## Installation & Setup

### Prerequisites
*   Node.js (v18.0.0 or higher)

### 1. Installation
Install packages:
```bash
cd frontend
npm install
```

### 2. Local Launch
Spin up the Vite React server:
```bash
npm run dev
```

Open `http://localhost:5173/` in your browser.

---

## Test Accounts
You can log in instantly using the **quick autofill buttons** on the Sign In page, or enter the credentials manually:

*   **Test Regular User**: 
    *   *Email*: `user@mediahub.com`
    *   *Password*: `user123`
*   **Test Administrator**: 
    *   *Email*: `admin@mediahub.com`
    *   *Password*: `admin123`
