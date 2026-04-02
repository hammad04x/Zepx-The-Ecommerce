<div align="center">

<img src="https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React"/>
<img src="https://img.shields.io/badge/Node.js-20-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js"/>
<img src="https://img.shields.io/badge/Express.js-4-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express"/>
<img src="https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL"/>
<img src="https://img.shields.io/badge/Razorpay-Integrated-02042B?style=for-the-badge&logo=razorpay&logoColor=white" alt="Razorpay"/>
<img src="https://img.shields.io/badge/Google_Auth-Enabled-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Google Auth"/>

<br/><br/>

# 🛍️ Zepx — The E-Commerce Platform

### A modern, full-stack e-commerce web application with React frontend, Node.js/Express REST API, MySQL database, Razorpay payment gateway, Google OAuth, and a full Admin Dashboard.

<br/>

[![GitHub Stars](https://img.shields.io/github/stars/hammad04x/Zepx-The-Ecommerce?style=social)](https://github.com/hammad04x/Zepx-The-Ecommerce/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/hammad04x/Zepx-The-Ecommerce?style=social)](https://github.com/hammad04x/Zepx-The-Ecommerce/network/members)
[![GitHub Issues](https://img.shields.io/github/issues/hammad04x/Zepx-The-Ecommerce)](https://github.com/hammad04x/Zepx-The-Ecommerce/issues)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Screenshots](#-screenshots)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Running the App](#-running-the-app)
- [API Endpoints](#-api-endpoints)
- [Database Schema](#-database-schema)
- [Author](#-author)

---

## 🌟 Overview

**Zepx** is a production-ready, full-stack e-commerce platform built to simulate a real-world online shopping experience. It features a fully responsive React storefront, a secure Express.js REST API, Razorpay payment gateway integration, Google OAuth login, and a powerful admin dashboard for product and order management.

The platform is designed with a focus on:
- Clean REST API design with Express.js
- Responsive, component-driven UI with React
- Secure authentication via JWT & Google OAuth
- Real payment flow with Razorpay
- Persistent relational data storage with MySQL
- Admin-only dashboard for full store control

---

## 📸 Screenshots

### 🏠 Home Page — SmartWatches Section
![Home Page](https://jagaralahammad.vercel.app/assets/zepx1-CHxpkP36.png)

---

### 🔍 Products Page — Category & Search Filter
![Products Page](https://jagaralahammad.vercel.app/assets/zepx2-CGaoMDds.png)

---

### 📦 Product Details
![Product Details](https://jagaralahammad.vercel.app/assets/zepx3-8a9rjsPk.png)

---

### 🛒 Add to Cart
![Cart Page](https://jagaralahammad.vercel.app/assets/zepx4-Bcjy5xkQ.png)

---

### 💳 Razorpay Payment Gateway
![Razorpay](https://jagaralahammad.vercel.app/assets/zepx5-FlUuLG79.png)

---

### 🔐 Login — Email/Password & Google OAuth
![Login Page](https://jagaralahammad.vercel.app/assets/zepx6-DDmn-ZWp.png)

---

### 🛠️ Admin Dashboard
![Admin Dashboard](https://jagaralahammad.vercel.app/assets/zepx7-CX8YK8vW.png)

---

### ➕ Admin — Add Product Page
![Add Product](https://jagaralahammad.vercel.app/assets/zepx8-iHVo5jSu.png)

---

## 🛠 Tech Stack

### 🖥️ Frontend — `client/`

| Technology | Role |
|---|---|
| ⚛️ **React** | UI Component Library |
| 🔀 **React Router DOM** | Client-side Routing |
| 🎨 **CSS3** | Custom Styling & Animations |
| 📦 **Axios** | HTTP Client for API calls |
| 🔵 **Google OAuth** | Social Login Integration |
| 💳 **Razorpay JS SDK** | Payment Checkout UI |

### ⚙️ Backend — `server/`

| Technology | Role |
|---|---|
| 🟢 **Node.js** | Runtime Environment |
| 🚂 **Express.js** | REST API Framework |
| 🐬 **MySQL** | Relational Database |
| 🔗 **mysql2** | MySQL Driver for Node |
| 🔐 **bcryptjs** | Password Hashing |
| 🪙 **JWT** | Authentication Tokens |
| 🔵 **Google Auth Library** | OAuth Token Verification |
| 💳 **Razorpay Node SDK** | Payment Order Creation & Verification |
| 🌐 **CORS** | Cross-Origin Resource Sharing |
| 📦 **dotenv** | Environment Configuration |

---

## 🏗 Architecture

```
┌──────────────────────────────────────────────────────────┐
│                     Browser / Client                      │
│         React App  ·  React Router  ·  Google OAuth       │
│              Razorpay Checkout  ·  Axios                  │
└───────────────────────────┬──────────────────────────────┘
                            │ HTTP REST API
┌───────────────────────────▼──────────────────────────────┐
│                    Express.js Server                      │
│  Auth Routes  ·  Product Routes  ·  Order Routes          │
│  JWT Middleware  ·  Admin Middleware  ·  Razorpay SDK      │
│  Google Auth Verify  ·  CORS  ·  Error Handler            │
└───────────────────────────┬──────────────────────────────┘
                            │ SQL (mysql2)
┌───────────────────────────▼──────────────────────────────┐
│                      MySQL Database                       │
│   users · products · categories · orders · order_items    │
│                       cart_items                          │
└──────────────────────────────────────────────────────────┘

                            +
┌──────────────────────────────────────────────────────────┐
│                   External Services                       │
│         💳 Razorpay API  ·  🔵 Google OAuth API           │
└──────────────────────────────────────────────────────────┘
```

---

## ✨ Features

### 🛒 Shopping Experience
- Browse products with category filters and search
- Product detail pages with full info
- Add to cart, update quantities, remove items
- Fully responsive UI for mobile and desktop

### 🔐 Authentication
- Email & password registration/login
- **Google OAuth** social login
- JWT-based session management
- Password hashing with bcrypt
- Protected routes on client and server

### 💳 Payments
- **Razorpay Payment Gateway** integration
- Order creation on backend, payment verification on callback
- Secure transaction flow end to end

### 📦 Order Management
- Place orders directly from cart
- Order history per user
- Order status tracking

### 🛠️ Admin Dashboard
- Dedicated admin-only interface
- Add, edit, delete products
- Manage product images, categories, pricing, stock
- View and manage all orders

---

## 📁 Project Structure

```
Zepx-The-Ecommerce/
├── client/                        # React Frontend
│   ├── public/
│   └── src/
│       ├── components/            # Reusable UI Components
│       ├── pages/                 # Route-level Pages
│       │   ├── Home.jsx
│       │   ├── Products.jsx
│       │   ├── ProductDetail.jsx
│       │   ├── Cart.jsx
│       │   ├── Login.jsx
│       │   └── admin/             # Admin Dashboard Pages
│       ├── context/               # Auth & Cart Context
│       ├── services/              # Axios API Helpers
│       ├── App.jsx
│       └── main.jsx
│
├── server/                        # Node.js/Express Backend
│   ├── config/
│   │   └── db.js                  # MySQL Connection Pool
│   ├── controllers/               # Route Logic
│   ├── routes/                    # Express Routers
│   │   ├── auth.js
│   │   ├── products.js
│   │   ├── cart.js
│   │   ├── orders.js
│   │   └── payment.js
│   ├── middleware/
│   │   ├── authMiddleware.js      # JWT Verification
│   │   └── adminMiddleware.js     # Admin Role Guard
│   └── index.js                   # Server Entry Point
│
├── .gitignore
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

```bash
🟢 Node.js 18+
🐬 MySQL 8.0+
📦 npm or yarn
💳 Razorpay Account (for payment keys)
🔵 Google Cloud Project (for OAuth credentials)
```

### Clone the Repository

```bash
git clone https://github.com/hammad04x/Zepx-The-Ecommerce.git
cd Zepx-The-Ecommerce
```

### Setup the Database

```sql
CREATE DATABASE zepx_db;
```

### Configure Environment Variables

Create a `.env` file inside `server/`:

```env
PORT=5000

# Database
DB_HOST=localhost
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
DB_NAME=zepx_db

# JWT
JWT_SECRET=your_super_secret_key

# Razorpay
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret

# Google OAuth
GOOGLE_CLIENT_ID=your_google_client_id
```

---

## ▶️ Running the App

### Backend

```bash
cd server
npm install
npm start        # with nodemon (recommended)
# or
node index.js
```

> Server runs at: `http://localhost:5000`

### Frontend

```bash
cd client
npm install
npm run dev        # Vite
# or
npm start          # CRA
```

> Client runs at: `http://localhost:5173` or `http://localhost:3000`

> ⚠️ Run both `client` and `server` simultaneously for the app to work.

---

## 🔌 API Endpoints

### 🔐 Auth

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/auth/register` | Register with email & password |
| `POST` | `/api/auth/login` | Login & receive JWT |
| `POST` | `/api/auth/google` | Google OAuth login |

### 📦 Products

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/products` | Get all products |
| `GET` | `/api/products/:id` | Get product by ID |
| `GET` | `/api/products?category=X&search=Y` | Filter & search |
| `POST` | `/api/products` | Add product *(admin only)* |
| `PUT` | `/api/products/:id` | Update product *(admin only)* |
| `DELETE` | `/api/products/:id` | Delete product *(admin only)* |

### 🛒 Cart

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/cart` | Get user's cart |
| `POST` | `/api/cart` | Add item to cart |
| `PUT` | `/api/cart/:id` | Update quantity |
| `DELETE` | `/api/cart/:id` | Remove cart item |

### 📋 Orders

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/orders` | Get user's orders |
| `POST` | `/api/orders` | Place a new order |
| `GET` | `/api/orders/:id` | Get order details |

### 💳 Payment

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/payment/create-order` | Create Razorpay order |
| `POST` | `/api/payment/verify` | Verify payment signature |

---

## 🗃 Database Schema

```
┌─────────────┐       ┌──────────────┐       ┌─────────────┐
│    users    │       │   products   │       │  categories │
│─────────────│       │──────────────│       │─────────────│
│ id          │       │ id           │◄──────│ id          │
│ name        │       │ name         │       │ name        │
│ email       │       │ description  │       └─────────────┘
│ password    │       │ price        │
│ google_id   │       │ image_url    │
│ role        │       │ category_id  │
│ created_at  │       │ stock        │
└──────┬──────┘       └──────┬───────┘
       │                     │
       │    ┌────────────┐   │
       │    │ cart_items │   │
       │    │────────────│   │
       └───►│ user_id    │   │
            │ product_id │◄──┘
            │ quantity   │
            └────────────┘
       │
       │    ┌────────────────┐     ┌──────────────┐
       │    │     orders     │     │ order_items  │
       │    │────────────────│     │──────────────│
       └───►│ id             │────►│ order_id     │
            │ user_id        │     │ product_id   │
            │ total          │     │ quantity     │
            │ status         │     │ price        │
            │ razorpay_pay_id│     └──────────────┘
            │ created_at     │
            └────────────────┘
```

---

## 👨‍💻 Author

<div align="center">

**Hammad**

[![GitHub](https://img.shields.io/badge/GitHub-hammad04x-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/hammad04x)
[![Portfolio](https://img.shields.io/badge/Portfolio-Live-00C7B7?style=for-the-badge&logo=vercel&logoColor=white)](https://jagaralahammad.vercel.app)

*Crafting full-stack experiences — from REST APIs to pixel-perfect UIs*

</div>

---

<div align="center">

⭐ **Found this useful? Star the repo and spread the word!** ⭐

</div>
