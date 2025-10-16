# Handicraft Toys E-commerce Platform

A full-stack web app for browsing, filtering, and purchasing unique handicraft toys.

<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/ae57fb58-3446-4f63-9597-63f1695d45f1" />

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
json
{
  "name": "Handmade Wooden Elephant",
  "description": "A beautifully crafted wooden elephant toy.",
  "price": 25.99,
  "image": "https://your-image-host/elephant.jpg",
  "category": "Animals"
}

# Alaiy E-commerce App 🛍️

A full-stack e-commerce platform for browsing, filtering, and purchasing unique handicraft toys.


## 🚀 Tech Stack

![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwind-css&logoColor=white)
![ShadCN UI](https://img.shields.io/badge/ShadCN_UI-FF6F61?style=flat)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat&logo=stripe&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat&logo=json-web-tokens&logoColor=white)


## ✨ Features

- 🛒 Product browsing and filtering  
- 🧑 User authentication with JWT  
- 💳 Stripe payment integration (test mode)  
- 📦 Cart management and checkout  
- 🔄 Responsive design with Tailwind CSS  
- 🖼️ ShadCN UI components for consistent UI  


## 📸 Screenshots

![Homepage Screenshot](assets/home.png)  
![Product Page Screenshot](assets/product.png)  
![Cart Screenshot](assets/cart.png)  
![Checkout Screenshot](assets/checkout.png)

/><img width="894" height="1024" alt="cart Image Oct 16, 2025, 04_57_59 PM" src="https://github.com/user-attachments/assets/e6f4621d-3333-4d68-bd76-6a34bd0f7e98" />

## 🧠 System Architecture

<img width="1536" height="853" alt="flow Image Oct 16, 2025, 04_53_02 PM" src="https://github.com/user-attachments/assets/6c5b6169-ebf9-46ae-aaac-33775e20f165" />
🧠 System Architecture Overview

The Alaiy Handicraft E-commerce Platform follows a modular full-stack architecture that ensures scalability, security, and maintainability.
It is designed to provide a seamless experience from browsing handcrafted products to secure payment checkout.

🔍 Architecture Highlights

Frontend (React + Tailwind + ShadCN UI)
Handles user interactions, dynamic routing, and product visualization.
Communicates with the backend via RESTful APIs for authentication, product data, and payments.

Backend (Node.js + Express)
Acts as the core server managing routes, middleware, authentication, and payment processing.
Uses JWT tokens for secure user sessions and bcrypt for password hashing.

Database (MongoDB Atlas)
Stores product details, user profiles, cart items, and order histories.
Optimized with indexes for fast querying and scalability.

Payment Gateway (Stripe API)
Integrates secure payment processing for test mode transactions.
Handles payment confirmation and order status updates.

Deployment

Frontend → Vercel / Netlify

Backend → Render / Heroku / Vercel / AWS Lambda

🏗️ Data Flow Summary

User Interaction:
User signs up or logs in from the React frontend.

API Communication:
Frontend sends API requests to the Node.js backend for authentication or product data.

Database Operations:
Backend fetches or updates records in MongoDB as needed.

Cart & Checkout:
Selected products are added to the cart and processed via Stripe API.

Payment Confirmation:
Stripe returns payment success/failure; backend stores order details in the database.

Frontend Update:
User receives visual confirmation and order summary after successful checkout.
⚙️ Setup Instructions

## 🔐 Authentication

Users can sign up, log in, and log out

JWT tokens are used for session management

Passwords are securely hashed using bcrypt

## 💳 Stripe Integration

Test mode payments enabled via Stripe API

Supports card checkout for products

Payment status handled and updated in backend

## 🚀 Deployment

Deploy backend on Render / Heroku

Deploy frontend on Vercel / Netlify

Update frontend .env to point to your deployed backend API

Update Stripe keys to production keys before going live

## 🤝 Contributing

Fork the repository

Create a new branch (git checkout -b feature/YourFeature)

Make your changes and commit (git commit -m "Add some feature")

Push to the branch (git push origin feature/YourFeature)

Open a Pull Request


## 🧩 Backend Setup

cd backend
npm install
cp .env.example .env   # Add your MongoDB URI, JWT_SECRET, and Stripe keys
npm run dev            # Starts backend server on localhost:5000

🎨 Frontend Setup
cd frontend
npm install
npm start              # Runs React app on localhost:3000

## 🗂️ Folder Structure
```bash
ecommerce-handicraft-toys/
├── backend/
│   ├── controllers/           # (Optional, for splitting business logic)
│   ├── models/
│   │   ├── Product.js
│   │   └── User.js
│   ├── routes/
│   │   ├── auth.js
│   │   ├── cart.js
│   │   ├── payment.js
│   │   └── product.js
│   ├── utils/                 # (Optional, for helpers)
│   ├── config/                # (Optional, for DB config)
│   ├── app.js
│   ├── package.json
│   └── .env
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── assets/            # (Product images, etc.)
│   │   ├── components/
│   │   │   └── ProductCard.js
│   │   ├── context/
│   │   │   ├── AuthContext.js
│   │   │   └── CartContext.js
│   │   ├── pages/
│   │   │   ├── Cart.js
│   │   │   ├── Checkout.js
│   │   │   ├── Home.js
│   │   │   ├── Login.js
│   │   │   ├── Signup.js
│   │   │   └── ProductDetail.js
│   │   ├── App.js
│   │   ├── index.js
│   │   └── tailwind.config.js
│   ├── package.json
│
├── README.md
└── .gitignore


