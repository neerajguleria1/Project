# Teacher Portfolio & Blog Platform

Full-stack MERN application with blog management system.

## Features
- Blog posts with multiple images
- Admin panel for content management
- Contact form
- Responsive design

## Tech Stack
- **Frontend:** React, TypeScript, Vite, TailwindCSS
- **Backend:** Node.js, Express, MongoDB
- **Deployment:** Docker

## Setup

### Using Docker (Recommended)

1. Clone the repository
```bash
git clone <your-repo-url>
cd project
```

2. Create environment files
```bash
cp server/.env.example server/.env
cp client/.env.example client/.env
```

3. Update `.env` files with your credentials

4. Run with Docker
```bash
docker-compose up --build
```

Access:
- Client: http://localhost:4173
- Server: http://localhost:5000

### Manual Setup

**Server:**
```bash
cd server
npm install
npm start
```

**Client:**
```bash
cd client
npm install --legacy-peer-deps
npm run dev
```

## Environment Variables

### Server (.env)
- `PORT` - Server port (default: 5000)
- `MONGO_URI` - MongoDB connection string

### Client (.env)
- `VITE_API_URL` - Backend API URL
- `VITE_CONTACT_API_URL` - Contact API URL
- `VITE_ADMIN_PASSWORD` - Admin login password
- `VITE_SUPABASE_ANON_KEY` - Supabase key (if using)
- `VITE_SUPABASE_URL` - Supabase URL (if using)

## Deployment

Update client `.env` with production URLs before building.
