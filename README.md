# Road Safety Expert System

A full-stack application that provides road safety intervention recommendations using AI and official guidelines.

## Project Structure

```
Road-Safety-GPT/
├── frontend/              # Main application 
│   ├── api/              # Serverless API functions
│   ├── src/              # React application
│   ├── road_safety_interventions.csv
│   └── vercel.json       # Vercel configuration
└── README.md
```

## Quick Start

### Local Development

```bash
cd frontend
npm install
npm run dev
```



## Features

- AI-powered road safety analysis using Google Gemini
- CSV-based intervention database
- React frontend with Vite
- Serverless API on Vercel
- PDF report generation
- QR code sharing

## Tech Stack

- **Frontend**: React, Vite, TailwindCSS
- **Backend**: Vercel Serverless Functions
- **AI**: Google Gemini API
- **Database**: CSV file with road safety interventions

## Environment Variables

Create a `.env` file in the `frontend` directory:

```
GEMINI_API_KEY=your_gemini_api_key_here
```

## License

MIT

