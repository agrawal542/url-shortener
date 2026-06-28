# 🚀 URL Shortener (Express + TypeScript + tRPC + MongoDB + Redis)

A modern URL shortener built using **Express**, **TypeScript**, **tRPC**, **MongoDB**, and **Redis** with a clean layered architecture (Controller → Service → Repository).

---

## ⚙️ Tech Stack

- Node.js
- Express.js
- TypeScript
- tRPC (end-to-end type safety)
- MongoDB + Mongoose
- Redis (counter + caching)
- Zod (validation)

---

## 📦 Project Setup

### 1. Clone the project

git clone https://github.com/singhsanket143/Express-Typescript-Starter-Project.git url-shortener

---

### 2. Move into project directory

cd url-shortener

---

### 3. Install dependencies

npm install

---

### 4. Create `.env` file

touch .env

Add:

PORT=3000
MONGO_URI=mongodb://localhost:27017/short_my_url
REDIS_URL=redis://localhost:6379
REDIS_COUNTER_KEY=url_shortener_counter
BASE_URL=http://localhost:3000

---

### 5. Run project

npm run dev

---

## 🧠 Install tRPC

npm install @trpc/server @trpc/client @trpc/express zod

---

## 🔗 API (tRPC)

### Create Short URL (mutation)

createShortUrl({
  originalUrl: "https://google.com"
})

---

### Get Original URL (query)

getOriginalUrl({
  shortUrl: "abc123"
})

---

## 🏗 Architecture

Client
  ↓
tRPC Router
  ↓
Service Layer
  ↓
Repository Layer
  ↓
MongoDB + Redis

---

## 🔥 Features

- Base62 short URL generation
- Redis counter for fast unique IDs
- MongoDB persistence
- Cached URL lookups
- Clean service-repository architecture
- Fully type-safe APIs with tRPC

---

## 🚀 Flow

Request → tRPC → Service → Redis (ID) → Base62 → MongoDB → Response

---

## 🧪 Run Services

brew services start mongodb/brew/mongodb-community@8.2
brew services start redis

---

## 📌 Done 🎉