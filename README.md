# NoteX Server

Backend server for NoteX application.

## Setup

1. Install dependencies:
```bash
npm install
```

2. Create a `.env` file in the server directory:
```
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key_here
GEMINI_API_KEY=your_gemini_api_key_here
PORT=5000
```

3. Start the server:
```bash
npm start
```

For development with auto-reload:
```bash
npm run dev
```

## API Endpoints

### Authentication
- POST `/api/auth/register` - Register new user
- POST `/api/auth/login` - Login user
- GET `/api/auth/profile` - Get user profile
- PUT `/api/auth/profile` - Update user profile

### Notes
- GET `/api/notes` - Get all notes
- GET `/api/notes/:id` - Get single note
- POST `/api/notes` - Create note
- POST `/api/notes/upload` - Upload PDF note
- PUT `/api/notes/:id` - Update note
- DELETE `/api/notes/:id` - Delete note

### Chat
- POST `/api/chat/:noteId` - Chat with note
- GET `/api/chat/:noteId/history` - Get chat history
- GET `/api/chat/stats/conversations` - Get conversations count

### Quick Notes
- GET `/api/quicknotes` - Get all quick notes
- POST `/api/quicknotes` - Create quick note
- PUT `/api/quicknotes/:id` - Update quick note
- DELETE `/api/quicknotes/:id` - Delete quick note

### Dashboard
- GET `/api/dashboard/stats` - Get dashboard statistics

### AI Actions
- POST `/api/ai/action` - Perform AI action (summarize, quiz, explain, flashcards)

