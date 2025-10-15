# E-commerce-app

# Handicraft Toys E-commerce Platform

A full-stack web app for browsing, filtering, and purchasing unique handicraft toys.

## Tech Stack
- Frontend: React.js, Tailwind CSS, ShadCN UI, Stripe
- Backend: Node.js, Express, MongoDB
- Authentication: JWT
- Payments: Stripe (test mode)
- Deployment: Vercel/Netlify/Render

## Features
- User authentication (sign up/login)
- Browse toys, filter by category
- Add/remove in cart, checkout with Stripe
- Mobile-optimized, vintage/retro theme

## Getting Started

1. Clone repo
2. Install dependencies in `/backend` and `/frontend`
   - `npm install`
3. Add `.env` file in `/backend` (see sample)
4. Start backend: `npm start` in `/backend`
5. Start frontend: `npm start` in `/frontend`
6. Frontend runs on `localhost:3000`, backend on `localhost:5000`

## Sample Product Data

Seed products using POST `/api/products` with JSON like:
```json
{
  "name": "Handmade Wooden Elephant",
  "description": "A beautifully crafted wooden elephant toy.",
  "price": 25.99,
  "image": "https://your-image-host/elephant.jpg",
  "category": "Animals"
}
```
