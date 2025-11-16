# Road Safety Expert System - Frontend

AI-powered road safety intervention recommendation system built with React and Vite.

## Quick Start

### 1. Install Dependencies

```bash
npm install
```

### 2. Set Up Environment Variables

Copy `.env.example` to `.env` and add your Gemini API key:

```bash
cp .env.example .env
```

Edit `.env` and add your key:

```
GEMINI_API_KEY=your_actual_api_key_here
```

### 3. Run Development Server

```bash
npm run dev
```

This will start:
- Vite dev server on http://localhost:5173 (frontend)
- Express API server on http://localhost:3001 (backend for local dev)

Visit http://localhost:5173 in your browser


## Project Structure

```
frontend/
├── api/                  # Vercel serverless functions
│   └── generate-report.js
├── src/                  # React application
│   ├── components/
│   ├── App.jsx
│   └── main.jsx
├── road_safety_interventions.csv  # Database
└── vercel.json          # Vercel configuration
```

## Features

- AI-powered analysis using Google Gemini
- CSV-based intervention database
- PDF report generation
- QR code sharing
- Responsive design with TailwindCSS
- Serverless API on Vercel

## Tech Stack

- React 18
- Vite
- TailwindCSS
- Google Gemini AI
- Vercel Serverless Functions
- React Router DOM
- QR Code generation

## Development

The app uses Vite for fast development and hot module replacement. 

**Local Development:**
- `npm run dev` runs both Vite (port 5173) and a local Express server (port 3001)
- The Express server (`server-dev.js`) mimics the Vercel serverless function for local testing

**Production (Vercel):**
- API routes are handled by Vercel serverless functions in the `api/` directory
- No Express server needed - Vercel handles everything

## Building for Production

```bash
npm run build
```

This creates an optimized production build in the `dist/` directory.
