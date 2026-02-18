# Deployment Guide

## Local Docker Setup

1. Make sure Docker is installed
2. Update `server/.env` with your MongoDB URI
3. Run: `docker-compose up --build`

## Production Deployment

### For Render/Railway/Heroku:

**Server:**
- Set environment variable: `MONGO_URI`
- Build command: `npm install`
- Start command: `npm start`
- Port: 5000

**Client:**
- Set environment variables:
  - `VITE_API_URL=https://your-server-url.com/api/blogs`
  - `VITE_CONTACT_API_URL=https://your-server-url.com/api/contact`
  - `VITE_ADMIN_PASSWORD=your_password`
- Build command: `npm install --legacy-peer-deps && npm run build`
- Start command: `npm run preview`
- Port: 4173

### Important Notes:
1. Update `VITE_API_URL` in client `.env` to your production server URL
2. Whitelist your deployment IP in MongoDB Atlas
3. Keep `.env` files secure (never commit to Git)
