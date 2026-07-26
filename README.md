<div align="center">

# 🍕 Foodie — Full-Stack Food Ordering Web Application

A full-stack food ordering web application built with **React, Express.js, and Supabase**, featuring protected admin login, category-based food browsing, a shopping cart with context-based state management, order placement with WhatsApp confirmation, and an admin order management panel.

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![WhatsApp](https://img.shields.io/badge/WhatsApp_Notification-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)

</div>

---

## 📖 Overview

**Foodie** is a full-stack food ordering web application built with a **React (Vite)** frontend and an **Express.js** backend, connected through REST APIs, with **Supabase** used for data storage.

The application includes a protected admin login system, a food browsing interface with categories (Pizza, Burger, Fries, and more), a shopping cart powered by React Context, order placement with an automated **WhatsApp order confirmation message**, and an admin panel to view and delete all placed orders.

---

## 🔄 Application Flow

```text
Admin Login (User ID + Password)
        ↓
Protected Route
        ↓
React Frontend (Home Page)
        ↓
Explore Categories
        ↓
View Food Items (Pizza / Burger / Fries)
        ↓
Add to Cart (Cart Context)
        ↓
Cart Page (Name, Address, Phone, Quantity)
        ↓
Place Order
        ↓
Express.js Backend
        ↓
Order Stored in Supabase
        ↓
WhatsApp Order Confirmation Sent
        ↓
Order Confirmed
        ↓
All Booked Orders (View / Delete)
```

---

## 📸 Application Preview

<div align="center">

**Admin Login**

<img src="./Login.png" alt="Admin Login Page" width="100%">

<br><br>

**Home Page**

<img src="./Home.png" alt="Home Page" width="100%">

<br><br>

**Explore Categories**

<img src="./Categories.png" alt="Explore Categories" width="100%">

<br><br>

**Category — Food Listing**

<img src="./Pizza.png" alt="Pizza Category Listing" width="100%">

<br><br>

**Cart Page**

<img src="./Cart.png" alt="Cart Page" width="100%">

<br><br>

**Order Confirmed**

<img src="./OrderConfirmed.png" alt="Order Confirmation Popup" width="100%">

<br><br>

**All Booked Orders (Admin Panel)**

<img src="./AllOrders.png" alt="All Booked Orders" width="100%">

</div>

---

## 🔐 Admin Login & Protected Routes

The application starts with an **Admin Login** page requiring a **User ID** and **Password**.

- Admin credentials are stored separately in **Supabase**.
- A `ProtectedRoute` component guards application routes, allowing access only after a valid login.

---

## 🧩 Frontend

The frontend is built with **React** and **Vite**, structured into components, pages, context, and CSS modules.

### Components

| Component | Description |
|---|---|
| **LOGINPAGE** | Admin login screen with User ID and Password fields |
| **ProtectedRoute** | Restricts access to routes until admin is logged in |
| **Navbar** | Branding, search bar, "All Orders" link, profile, and Sign Out |
| **AllOrdersNavbar** | Navbar used within the All Orders (admin) page |
| **Hero** | Highlights the featured/today's special item |
| **SearchBar** | Food search interface |
| **Categories** | Displays browsable food categories |
| **PizzaData** | Pizza category food items and data |
| **BurgerData** | Burger category food items and data |
| **FriesData** | Fries category food items and data |
| **Floatingcart** | Floating cart icon accessible across pages |
| **Cart** | Cart page with customer details, quantity controls, and total |
| **PastOrders** | Displays previously booked orders |
| **BurgerOrders** | Displays order-related data for the Burger category |
| **Supabase** | Supabase client configuration and API calls |

### Pages

| Page | Description |
|---|---|
| **Home** | Landing page with Hero and Categories |
| **Pizza** | Pizza category listing page |
| **Burger** | Burger category listing page |
| **Fries** | Fries category listing page |
| **AllOrders** | Admin page listing all booked orders with delete option |

### State Management

- **CartContext** — Manages cart items, quantities, and totals across the application using React Context.

---

## ⚙️ Backend

The backend is built with **Node.js** and **Express.js**, acting as the API layer between the React frontend and Supabase.

```text
React Frontend
      ↓
Express.js Backend
      ↓
REST API
      ↓
Supabase (Orders + Admin Credentials)
      ↓
WhatsApp Notification Service
```

**Backend Responsibilities:**

- Handling order creation, update, and deletion requests
- Storing order data in **Supabase**
- Storing and verifying admin login credentials in **Supabase**
- Sending an automated **WhatsApp order confirmation message** once an order is successfully placed
- Deleting orders from **Supabase** when removed from the admin panel

---

## 🔌 API Operations

| Method | Operation | Purpose |
|---|---|---|
| POST | Create Order | Places a new order and stores it in Supabase |
| DELETE | Delete Order | Deletes an order from Supabase |

---

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| Frontend | React.js, Vite, JavaScript, HTML, CSS |
| Backend | Node.js, Express.js |
| API | REST APIs |
| Database / Services | Supabase |
| State Management | React Context API |
| Notifications | WhatsApp Order Confirmation |
| API Testing | Postman |
| Development Tools | Git, GitHub |

---

## ✨ Key Features

- 🔐 Protected admin login with credentials stored in Supabase
- 🛡️ Route protection using `ProtectedRoute`
- 🍽️ Category-based food browsing (Pizza, Burger, Fries)
- 🍔 Food listing with images, pricing, and "Add to Cart"
- 🔍 Search interface
- 🛒 Cart management via React Context (`CartContext`)
- 📝 Order placement form with name, address, and phone number
- ✅ Order confirmation popup on successful order placement
- 💬 Automated WhatsApp order confirmation message
- 🗄️ Orders stored and managed in Supabase
- 📋 Admin panel (`AllOrders`) to view all booked orders
- 🗑️ Delete orders from the admin panel (removed from Supabase in real time)
- 🔌 Express.js REST API backend

---

## 📁 Project Structure

```text
Foodie/
│
├── public/
│
├── src/
│   ├── assets/
│   │   ├── cheesyfries.png
│   │   ├── ChickenCheeseBurstBurger.png
│   │   ├── CrispyChickenBurger.png
│   │   ├── east rosted veggie pizza.png
│   │   ├── FrenchFries.png
│   │   ├── GreenChilliVeggieBurger.png
│   │   ├── hero.png
│   │   ├── idli.png
│   │   ├── LoadedFries.png
│   │   ├── NavbarBG.png
│   │   ├── PaneerTikkiBurger.png
│   │   ├── pizza1.png ... pizza6.png
│   │   ├── Profile.png
│   │   ├── react.svg
│   │   └── vite.svg
│   │
│   ├── Components/
│   │   ├── AllOrdersNavbar.jsx
│   │   ├── BurgerData.jsx
│   │   ├── BurgerOrders.jsx
│   │   ├── Cart.jsx
│   │   ├── Categories.jsx
│   │   ├── Floatingcart.jsx
│   │   ├── FriesData.jsx
│   │   ├── Hero.jsx
│   │   ├── LOGINPAGE.jsx
│   │   ├── Navbar.jsx
│   │   ├── PastOrders.jsx
│   │   ├── PizzaData.jsx
│   │   ├── ProtectedRoute.jsx
│   │   ├── SearchBar.jsx
│   │   └── Supabase.jsx
│   │
│   ├── Context/
│   │   └── CartContext.jsx
│   │
│   ├── CSS/
│   │   ├── AllOrderNavbar.css
│   │   ├── BurgerPage.css
│   │   ├── Cart.css
│   │   ├── Categories.css
│   │   ├── Floatingcart.css
│   │   ├── FriesPage.css
│   │   ├── Hero.css
│   │   ├── LOGINPAGE.css
│   │   ├── Navbar.css
│   │   ├── PastOrders.css
│   │   └── pizza.css
│   │
│   ├── Pages/
│   │   ├── AllOrders.jsx
│   │   ├── Burger.jsx
│   │   ├── Fries.jsx
│   │   ├── Home.jsx
│   │   └── Pizza.jsx
│   │
│   ├── App.css
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
│
├── backend/
│   ├── server.js
│   └── routes/
│
├── Login.png
├── Home.png
├── Categories.png
├── Pizza.png
├── Cart.png
├── OrderConfirmed.png
├── AllOrders.png
│
└── README.md
```

---

## 🚀 Future Improvements

- User-facing authentication (beyond admin login)
- Payment gateway integration
- Order status tracking
- Restaurant management features
- Production deployment

---

## 🎯 Project Objective

The objective of this project is to build a full-stack food ordering web application demonstrating:

- React frontend development with reusable components and pages
- Context API-based cart state management
- Protected route implementation for admin access
- Node.js and Express.js backend development
- REST API implementation
- Supabase integration for order and credential storage
- Automated WhatsApp order confirmation notifications
- Admin-side order management (view and delete)

---

## 👤 Author

**Shubham Gupta**

AI Automation Engineer | AI Agents | n8n | Full-Stack Development

---
