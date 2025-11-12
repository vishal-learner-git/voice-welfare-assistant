# voice-welfare-assistant
A multilingual AI voice assistant that helps citizens discover and access government welfare schemes using speech — built with Express, React, Drizzle ORM, and Whisper.
✨ Features
🔧 Backend

RESTful API powered by Express.js

Session-based authentication using Passport.js

Input validation with Zod

PostgreSQL database managed via Drizzle ORM

🎨 Frontend

Modern UI built with React + Vite

Tailwind CSS for utility-first styling

ShadCN/UI + Radix UI for accessible, composable components

React Hook Form for seamless form handling and validation

🧠 Voice Assistant Add-on (Hackathon Feature)

Speech-to-Text using OpenAI Whisper (Offline) or Google STT

Text-to-Speech (Tamil & Hindi) using Coqui / Google TTS

Basic eligibility logic for scheme recommendations

Works offline (Whisper-based) for rural accessibility

🛠 Tech Stack
Category	Technology	Purpose
Backend	Express.js, tsx	Server-side API and routing
Frontend	React, Vite	Client UI
Database	PostgreSQL 16, Drizzle ORM	Persistent data and schema migration
Sessions	express-session, connect-pg-simple	User sessions stored in PostgreSQL
Styling	Tailwind CSS, Shadcn/ui, Radix UI	Modern, responsive UI
Auth	Passport.js (local strategy)	Secure session-based login
Validation	Zod	Strong runtime validation
Forms	React Hook Form	Client-side form state
Environment	Replit	Hosted development environment
📁 Project Structure
.
├── client/               # React + Vite frontend
│   ├── src/
│   └── index.html
├── dist/                 # Production build output
├── migrations/           # Drizzle ORM migration files
├── server/               # Express.js backend
│   └── index.ts          # Server entry point
├── shared/               # Shared schema and utilities
│   └── schema.ts
├── components.json       # Shadcn/UI configuration
├── drizzle.config.ts     # Drizzle ORM config
├── package.json          # Scripts and dependencies
├── tailwind.config.ts    # Tailwind configuration
├── tsconfig.json         # TypeScript configuration
├── vite.config.ts        # Vite build setup
└── .replit               # Replit environment configuration

🚀 Getting Started
🔹 Prerequisites

Node.js (v20 or later)

npm (or any compatible package manager)

PostgreSQL database instance

🔹 1. Clone and Install
git clone <repository-url>
cd rest-express
npm install

🔹 2. Configure Environment Variables

Create a .env file in your root directory:

DATABASE_URL="postgresql://USER:PASSWORD@HOST:PORT/DATABASE"


💡 If using Replit, set this in the Secrets tab instead of .env.

🔹 3. Setup Database

Push your Drizzle schema to the database:

npm run db:push

🔹 4. Run the App
Development (with Hot Reload)
npm run dev


This runs both:

Express server via tsx

Vite client (proxied by Express)

Production Build
# Build client and server
npm run build

# Start the production server
npm run start

🧾 Available Scripts
Script	Description
npm run dev	Start server in development mode with hot reload
npm run build	Build both client (Vite) and server (esbuild)
npm run start	Run production server
npm run check	Type-check entire project using TypeScript
npm run db:push	Apply Drizzle ORM migrations to database
🧠 Voice Agent Hackathon Add-ons
Feature	Description
🎙️ Speech-to-Text	Tamil/Hindi transcription via Whisper
🔈 Text-to-Speech	Voice response via Coqui or Google TTS
🧮 Scheme Matching	Rule-based eligibility engine
💾 Offline Mode	Whisper-powered local transcription
🧍 User Roles	Applicant / Advisor interface planned
🧩 Future Improvements

Integration with Bhashini API for government-supported multilingual STT/TTS

Conversational logic powered by LLMs

Form auto-filling with OCR document scanning

Android app deployment for offline use
