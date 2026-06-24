# 🍾 PegBazar — Legal Alcohol Home Delivery

> Premium spirits, delivered fast. A full-stack MERN application for legal alcohol home delivery.

## Quick Start

### Prerequisites
- Node.js 18+
- MongoDB Atlas account (or local MongoDB)
- Cloudinary account (for image uploads)

### Installation

1. Install all dependencies
```bash
npm run install:all
```

2. Backend setup
```bash
cd backend
cp .env.example .env
# Fill in your .env values (MONGO_URI, JWT_SECRET, CLOUDINARY_*)
```

3. Seed admin & demo data
```bash
npm run seed
```

4. Run both servers
```bash
# From root directory
npm run dev
```

Or run separately:
```bash
cd backend && npm run dev    # http://localhost:5000
cd frontend && npm run dev   # http://localhost:5173
```

### Environment Variables

**backend/.env**
- `MONGO_URI` — MongoDB connection string
- `JWT_SECRET` — Secret for JWT tokens
- `CLOUDINARY_*` — Cloudinary credentials
- `CLIENT_URL` — Frontend URL (http://localhost:5173)

## Default Credentials (after seeding)
- **Admin:** admin@pegbazar.com / admin123
- **Demo Customer:** demo@pegbazar.com / demo123

## Tech Stack
- **Frontend:** React 18, Vite, Tailwind CSS, Redux Toolkit, Three.js, Framer Motion
- **Backend:** Node.js, Express.js, MongoDB, Mongoose
- **Auth:** JWT + bcrypt
- **Storage:** Cloudinary

## Features
- 🍾 Premium dark UI with glassmorphism & Three.js 3D hero
- 👤 Multi-role auth (Customer, Vendor, Admin, Delivery)
- 🛒 Cart, checkout with state restriction checks
- 📦 Order tracking & vendor management
- 🔒 Age verification (21+) on signup & checkout
- 🚫 Restricted state enforcement (Gujarat, Bihar, etc.)

## API Health Check
```
GET http://localhost:5000/api/health
```
