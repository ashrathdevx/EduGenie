# EduGenie

An AI-powered study assistant built with Next.js and the Gemini API. Ask questions, get guided explanations, and attach a PDF or image for context.

## Features

- Ask study questions and receive step-by-step explanations
- Attach a PDF or a JPEG, PNG, or WebP image to a question
- Responsive chat interface with subject prompt suggestions
- Server-side Gemini API integration; the API key stays on the server
- Request validation and clear handling for common API errors

## Tech stack

- Next.js App Router
- React and TypeScript
- Tailwind CSS
- Google Gemini via `@google/genai`
- Lucide icons and Motion for UI details

## Getting started

### Requirements

- Node.js 20 or newer
- npm
- A Gemini API key

### Install

```bash
npm install
```

Create `.env.local` in the project root:

```env
GEMINI_API_KEY=your_gemini_api_key
GEMINI_MODEL=gemini-2.5-flash
```

`GEMINI_MODEL` is optional; when omitted, EduGenie uses `gemini-2.5-flash`. Never commit your real API key.

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## Upload limits

EduGenie accepts PDF, JPEG, PNG, and WebP files up to 8 MB. Questions can be up to 12,000 characters.

## Available scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the local development server |
| `npm run build` | Create a production build |
| `npm run start` | Start the production server |
| `npm run lint` | Run ESLint |

## Project structure

```text
src/
├── app/          # Application shell and page
├── api/chat/     # Gemini-backed chat endpoint
├── components/   # Chat UI components
└── lib/          # Gemini client helpers and utilities
```

## Current scope

EduGenie is an early-stage project. Conversation history is held in the current session UI and is not persisted to a database. Gemini responses can be incorrect; review important answers against trusted course materials.

## License

No license has been added yet. Contact the repository owner before reusing this project.
