# Auth Backend (Node.js + Express + MongoDB + JWT)

A clean starter authentication API for your portfolio.

## Features
- Register and login with JWT
- Protected `/api/auth/me` route
- Password hashing with bcrypt
- Proper error handling
- CORS + JSON logging (morgan)

## Endpoints
- `POST /api/auth/register` → `{ name, email, password }`
- `POST /api/auth/login` → `{ email, password }`
- `GET /api/auth/me` (protected) → header `Authorization: Bearer <token>`

## Run Locally (Desktop or Termux on Android)
```bash
# 1) Install dependencies
npm install

# 2) Copy env
cp .env.example .env
# then edit .env and add your MONGO_URI and JWT_SECRET

# 3) Start (dev)
npm run dev
# or production
npm start
```

### Termux Quick Setup
```bash
pkg update && pkg upgrade -y
pkg install -y nodejs git
git clone <your-repo-url>.git auth-backend
cd auth-backend
npm install
cp .env.example .env && nano .env  # paste your MONGO_URI + JWT_SECRET
npm run dev
```

## Deploy (Free tiers)
- **Render.com**: New Web Service → Node → add env vars → build `npm install` → start `npm start`
- **Railway.app**: Deploy from GitHub → add env vars

## Notes
- Do not commit your real `.env`
- Change `JWT_SECRET` before going live
