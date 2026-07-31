# 🃏 Real-time Multi-User Memory Card Game ("Show" / Cabo / Golf)

[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black&style=flat-square)](#)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-4.0-38B2AC?logo=tailwind-css&logoColor=white&style=flat-square)](#)
[![Firebase](https://img.shields.io/badge/Firebase_Firestore-Cloud_DB-FFCA28?logo=firebase&logoColor=black&style=flat-square)](#)
[![NodeJS](https://img.shields.io/badge/NodeJS-Fullstack-339933?logo=node.js&logoColor=white&style=flat-square)](#)

A beautiful, high-fidelity, and fully responsive real-time **Memory Card Game** (popularly known as *Show*, *Cabo*, *Cambio*, or *Golf*). Play with physically nearby companions in Local mode, train your skills against tactical AI, or host live multiplayer lobby matches with real-time Firestore database synchronization!

---

## 📖 What is the Game?

The **Memory Card Game** is an engaging card-matching game of deduction, memory, timing, and strategy. 

Every player begins with **4 face-down cards** arranged in a 2x2 grid. Players do not know what cards they have, except for two they get to peek at during setup. The absolute ultimate goal is to **minimize your total point score** by swapping high-value cards for low-value ones, memory-tracking your secret grid, spying on opponents, and matching discarded cards to burn them away.

When you believe your total grid score is the lowest at the table, you call **"SHOW!"**. This gives every other competitor one last turn before all cards are revealed and scores are tallied!

---

## 🎮 Game Rules & Mechanics

### 🃏 Setup & Turn Actions
1.  **The Deal:** Each participant receives 4 cards face-down in a personal grid.
2.  **The Peek Phase:** Before turns begin, you can peek at **two** of your face-down cards. Memorize their values and positions well!
3.  **On Your Turn:**
    *   **Draw:** Draw one face-down card from the Deck **OR** pick up the top face-up card from the Discard Pile.
    *   **Action (Swap/Discard):** 
        *   If you drew from the Deck, you can swap it with any of your 4 grid cards (discarding the old one face-up) **OR** discard the drawn card directly to trigger its power.
        *   If you took the top Discard card, you *must* swap it into your grid and discard the card you replaced.

---

## ✨ Special Discard Powers
When you discard a card drawn from the deck, certain card values trigger immediate mystical powers:

*   **7 & 8:** **Peek** — Look at one of your own face-down grid cards.
*   **9 & 10:** **Spy** — Secretly view any one card in an opponent's grid.
*   **Jack & Queen:** **Blind Swap** — Exchange any two cards on the entire table without looking at them first.
*   **King:** **Spy & Swap** — Spy on any opponent's card, then choose whether to swap any two cards on the table.

---

## ⚡ Slap to Match (Burn Cards)
Whenever a card is thrown onto the Discard Pile, players can react quickly to match it!
*   If you (or any player) have a card in your grid that matches the value of the discarded card, tap **Match!** and select your card to **burn it away**!
*   **Success:** The card is permanently discarded, reducing your grid to fewer cards (and thus fewer points!).
*   **Fail:** Tapping "Match!" with an incorrect card triggers a penalty — you must draw an extra card, increasing your grid size!

---

## 📊 Card Points & Scoring
At the end of the round (after a "Show" call and final turns), all grid cards are flipped face-up. Players sum their card points:

| Card Type | Value / Point Value | Description |
| :--- | :--- | :--- |
| **Joker** | **-1 Point** | The ultimate card to hold! |
| **7** | **0 Points** | Free safe card. |
| **Red Kings** (♥/♦) | **0 Points** | Extremely valuable. |
| **Aces** | **1 Point** | Excellent low score. |
| **2 through 10** | **Face Value** | (e.g., a `5` is 5 points, a `10` is 10 points). |
| **Jacks & Queens** | **11 / 12 Points** | Dangerous high-scoring cards. |
| **Black Kings** (♠/♣) | **13 Points** | The worst penalty card in the deck! |

---

## 👑 Host Command Lobby & Customization
Host your own private or public rooms to play with up to **4 players**:
*   **Dynamic Lobby Slots:** Adjust room capacity (2, 3, or 4 players) on the fly.
*   **Tactical AI Bots:** Fill empty seats with bots featuring adjustable difficulties (**Easy**, **Medium**, **Hard**).
*   **Custom Match Settings:** Set Turn timers (**15s**, **30s**, **60s**, or **Unlimited**) to maintain tension.
*   **Card Themes:** Style your deck with premium visual themes:
    *   🃏 *Classic Standard*
    *   🔥 *Elemental Runes*
    *   👾 *Retro Pixel*
    *   🌌 *Cyber Neon*
*   **Server Regions:** Choose server affinity for your match (**US Server**, **Canada Server**, or **Global Matchmaking**).

---

## 🛠️ Installation & Getting Started

### Prerequisites
*   [Node.js](https://nodejs.org/) (v18+ recommended)
*   [npm](https://www.npmjs.com/)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/memory-game.git
   cd memory-game
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Configure your keys by placing a `firebase-applet-config.json` in the root folder with your credentials.
4. Run in developer mode:
   ```bash
   npm run dev
   ```
