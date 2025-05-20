

# 🛍️ PRINTFUSE

## 📋 Table of Contents
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Local Setup](#-local-setup)
  - [Backend Setup](#backend-setup)
  - [Frontend Setup](#frontend-setup)
- [Environment Variables](#-environment-variables)
- [Running the Application](#-running-the-application)
- [API Endpoints](#-api-endpoints)


## ✨ Features
- Seller registration/login with JWT
- Product CRUD operations
- WooCommerce integration
- Product sync status tracking

## 🛠 Tech Stack
**Frontend**: React.js (Vite), Material-UI  
**Backend**: Node.js, Express, Prisma  
**Database**: PostgreSQL  
**Auth**: JWT  

## 💻 Local Setup

### Backend Setup
1. Navigate to backend folder:
   ```bash
   cd backend

2. yarn install
3. npx prisma migrate dev --name init
#### Enviroment Variable Needed For Backend
1. DATABASE_URL="postgresql://postgres:password@localhost:5432/diploy?schema=public"
2. JWT_SECRET=your_jwt_secret_here
3. JWT_EXPIRES_IN=24h
4. WC_API_URL="https://yourstore.com/wp-json/wc/v3"
5. WC_CONSUMER_KEY=ck_your_key_here
6. WC_CONSUMER_SECRET=cs_your_secret_here

### Frontend Setup
1. Navigate to Frontend folder:
   ```bash
   cd ../frontend

2. yarn install
#### Enviroment Vairable Needed
   VITE_API_URL=http://localhost:8000/api

## Running the Application
1. Frontend By going in Frontend Directory
    ```bash
        cd backend
        node server.js
   
2. Backend By going in Backend Directory
    ```bash
        cd ../frontend
        yarn dev

## Api Endpoints
| Method | Endpoints          | Discription | Require Auth |
|--------|--------------------|-------------|--------------|
| Post   | /api/auth/register |             | No           |
| Post   | /api/auth/login    |             | No           |
| Get    | /api/products      |             | Auth         |
| Get    | /api/products/:id  |             | Auth         |
| Post   | /api/products      |             | Auth         |
| Put    | /api/products/:id  |             | Auth         |
| Delete | /api/products/:id  |             | Auth         |
