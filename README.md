# ChatGPT Clone

A full-stack AI chat application inspired by ChatGPT.
Users can create conversations, chat with AI models, and manage their chat history with authentication and database persistence.

## Live Demo

🔗 [https://chatgpt-clone-seven-psi.vercel.app/](https://chatgpt-clone-seven-psi.vercel.app/)

## Features

- 🔐 User authentication with Clerk
- 💬 AI-powered conversations
- 🗂️ Conversation history management
- ✨ ChatGPT-style interface
- 🌓 Dark/light theme support
- 📝 Markdown rendering for AI responses
- ⚡ Streaming AI responses
- 🗄️ Persistent data storage with PostgreSQL
- 🔄 Real-time conversation updates
- 📱 Responsive UI

## Tech Stack

### Frontend
- Next.js 16
- React 19
- TypeScript
- Tailwind CSS
- Shadcn UI
- Next Themes

### Backend
- Next.js Server Actions
- Next.js API Routes
- Prisma ORM

### Database
- PostgreSQL (Neon)

### Authentication
- Clerk Authentication

### AI Integration
- OpenAI API
- AI SDK

## Project Structure

```
chatgpt-clone/
│
├── app/
│   ├── api/
│   │   └── chat/
│   ├── (root)/
│   └── layout.tsx
│
├── components/
│   └── ui/
│
├── features/
│   ├── auth/
│   └── conversation/
│
├── lib/
│   ├── db.ts
│   └── generated/
│
├── prisma/
│   └── schema.prisma
│
└── public/
```

## Database Models

The application uses Prisma with PostgreSQL.

Main models:

### User
Stores authenticated user information synced from Clerk.

### Conversation
Stores chat sessions, titles, models, and metadata.

### Message
Stores individual user and AI messages.

## Environment Variables

Create a `.env` file:

```env
DATABASE_URL=

NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=

NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_IN_FALLBACK_REDIRECT_URL=/
NEXT_PUBLIC_CLERK_SIGN_UP_FALLBACK_REDIRECT_URL=/

OPENAI_API_KEY=
```

## Installation

Clone the repository:

```bash
git clone https://github.com/JustenAnas/chatgpt-clone.git
```

Navigate into the project:

```bash
cd chatgpt-clone
```

Install dependencies:

```bash
npm install
```

Generate Prisma client:

```bash
npx prisma generate
```

Run the development server:

```bash
npm run dev
```

Open in your browser:

```
http://localhost:3000
```

## Deployment

The project is deployed using:

- **Vercel** → Next.js application
- **Neon** → PostgreSQL database
- **Clerk** → Authentication
- **OpenAI** → AI responses

## Future Improvements

- Multiple AI model support
- File upload and document chat
- Voice conversations
- Chat sharing
- User settings
- Better conversation search
- AI memory system

## Author

**Anas Khan**
GitHub: [https://github.com/JustenAnas](https://github.com/JustenAnas)
