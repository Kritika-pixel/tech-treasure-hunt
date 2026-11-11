# 🏴‍☠️ Tech Treasure Hunt — The Lost Archives of Code

<p align="center">

  **Think. Decode. Solve. Conquer.**

  An interactive coding adventure where every challenge brings you closer to the treasure!

</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-18-blue?logo=react" />
  <img src="https://img.shields.io/badge/Node.js-Backend-green?logo=node.js" />
  <img src="https://img.shields.io/badge/PostgreSQL-Database-blue?logo=postgresql" />
  <img src="https://img.shields.io/badge/Status-Active-success" />
</p>

---

## 🌟 About The Project

**Tech Treasure Hunt** is an interactive, individual-player treasure hunt designed to make learning technology, programming, and logical thinking more exciting.

Players embark on a journey through five challenging levels, each featuring a different set of puzzles and problem-solving activities. From decoding mysterious scripts to identifying online scams, every stage tests a different skill.

But there's a twist!

Players must complete challenges while managing their time, collecting rewards, and maintaining focus throughout the adventure.

The ultimate goal? Complete all five levels, collect all five gems, and claim your place in the **Hall of Fame!**

## 🎮 The Five Levels

| Level | Challenge | What You'll Explore |
|---|---|---|
| 01 | 🔐 The Cipher Crypt | Decipher the Script |
| 02 | ⚙️ The Broken Machine | Repair What Was Corrupted |
| 03 | 🧩 Chamber of Riddles | Think Like the Ancients |
| 04 | 🕵️ Scam Sleuths | Spot the Fraud |
| 05 | 💻 Crack the Logic | Boolean Gates and Deduction |

Each level contains five questions, combining multiple-choice challenges, typed answers, and code-based problem solving.

## ✨ Key Features

- **Interactive Gameplay:** Five levels of technology-inspired challenges.
- **Single-Player Experience:** Every player gets an individual game session.
- **Time-Based Challenges:** Complete challenges while keeping track of your time.
- **Smart Penalty System:** Incorrect answers add 60 seconds to the player's time.
- **Coins & Gems:** Earn 10 coins for each correct answer and bonus rewards for completing levels.
- **Fullscreen Gameplay:** An immersive game experience with fullscreen support.
- **Focus Monitoring:** Tracks fullscreen exits, tab switching, and window focus events during active gameplay.
- **Hall of Fame:** Compete for recognition through a leaderboard based on completion time and penalties.
- **Secure Question Evaluation:** Correct answers remain on the server instead of being exposed to participants.
- **Persistent Progress:** Game rewards and player progress are stored in the database.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| React.js | Frontend user interface |
| Vite | Frontend development and build tool |
| Framer Motion | UI animations and transitions |
| Lucide React | Icons |
| Node.js | Backend runtime |
| Express.js | REST API |
| PostgreSQL | Database |
| JWT | Authentication |
| bcrypt | Password hashing |
| OpenAI API | AI integration |
| Zod | Data validation |

## 🏗️ Project Architecture

```text
tech-treasure-hunt/
│
├── client/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── ...
│   └── package.json
│
├── server/
│   ├── src/
│   │   ├── db/
│   │   ├── services/
│   │   └── ...
│   ├── seeds/
│   └── package.json
│
├── docker-compose.yml
├── package.json
└── README.md
```

## 🚀 Getting Started

Follow these steps to run the project locally.

### Prerequisites

Make sure you have installed:

- Node.js 20 or later
- npm
- PostgreSQL 14 or later (or Docker Desktop)
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/PurnimaRout06/tech-treasure-hunt.git
```

### 2. Navigate to the Project

```bash
cd tech-treasure-hunt/tech-treasure-hunt
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Configure Environment Variables

Copy the example environment file:

```powershell
Copy-Item .env.example server/.env
```

Configure the following variables in `server/.env`:

```env
DATABASE_URL=postgresql://postgres:local_dev_password@localhost:5432/tech_treasure_hunt

JWT_SECRET=your_secure_jwt_secret
COOKIE_SECRET=your_secure_cookie_secret
```

Use strong, unique secrets for your environment.

### 5. Start PostgreSQL

If you're using Docker:

```bash
docker compose up -d postgres
```

Alternatively, start your local PostgreSQL server.

### 6. Run Database Migrations

```bash
npm run db:migrate --workspace server
```

### 7. Import the Question Bank

```bash
npm run questions:import --workspace server -- ./seeds/approved-question-bank.json
```

### 8. Start the Backend

Open a terminal and run:

```bash
npm run dev:server
```

### 9. Start the Frontend

Open another terminal and run:

```bash
npm run dev:client
```

### 10. Open the Application

Visit:

**http://localhost:5173**

Backend health check:

**http://localhost:5000/api/health**

## 🏆 Reward System

The game rewards players for solving challenges and completing levels.

| Achievement | Reward |
|---|---|
| Correct Answer | 10 Coins |
| Complete All Questions in a Level | 25 Bonus Coins + 1 Gem |
| Complete All Five Levels | 5 Gems |

Incorrect answers do not earn rewards and add a 60-second penalty.

## ⏱️ Focus & Fair Play

To encourage fair gameplay, the application monitors certain browser focus events during an active attempt.

- Fullscreen exit events are recorded.
- Tab visibility changes are tracked.
- Window focus loss is logged.
- The default violation limit is three incidents.

**Note:** Browser-based monitoring is best-effort. It cannot completely prevent external assistance, switching devices, or other forms of cheating.

## 🔒 Security Considerations

- Passwords are hashed using bcrypt.
- Authentication uses JWT.
- Database credentials and secrets are managed through environment variables.
- Correct answers are kept in the server-side database.
- Question submissions are evaluated on the backend.
- Repeated submissions are protected against duplicate reward and penalty processing.

Never commit your `.env` file or expose private API keys.

## 🌐 Live Demo

Explore the deployed project:

**[Tech Treasure Hunt — Play Now](https://tech-treasure-hunt-swart.vercel.app/)**

## 🔮 Future Enhancements

Some ideas for expanding the experience:

- More challenging treasure-hunt levels.
- Multiplayer competitions and team-based challenges.
- Additional coding languages and programming puzzles.
- Advanced player statistics and achievements.
- More interactive animations and game environments.
- Expanded organizer controls and event analytics.

## 🤝 Contributing

Contributions, ideas, and suggestions are welcome!

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Commit your changes.
5. Submit a pull request.

## 💜 The Idea Behind the Game

Learning technology doesn't always have to mean reading documentation or solving ordinary exercises.

Sometimes, it can be an adventure.

**Every puzzle has a secret. Every level has a challenge. Every player has a treasure to find.**

---

<p align="center">
  <b>🏴‍☠️ Ready to begin your adventure?</b>
  <br/>
  <i>Decode the clues. Beat the clock. Find the treasure!</i>
</p>
