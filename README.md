# Auth API 2

A modern fullstack authentication API project with a Rust (Axum) backend and a React (TypeScript) frontend.

---

## 🚀 Project Overview
This project provides a secure, scalable authentication API with a beautiful, modern frontend. It is designed for learning, rapid prototyping, and as a foundation for production-ready auth systems.

- **Backend:** Rust + Axum (JWT, bcrypt, RESTful API)
- **Frontend:** React + TypeScript (responsive, glassmorphism UI)

---

## ✨ Features
- User registration & login
- JWT-based authentication
- Protected routes (admin, profile, etc.)
- Password hashing (bcrypt)
- Environment-based configuration
- Swagger/OpenAPI documentation
- Modern, professional UI (green & soft black theme)

---

## 🛠️ Tech Stack
- **Backend:** Rust, Axum, Tokio, bcrypt, jsonwebtoken, utoipa (OpenAPI)
- **Frontend:** React, TypeScript, Axios, React Router

---

## 📦 Getting Started

### Prerequisites
- [Rust](https://www.rust-lang.org/tools/install)
- [Node.js & npm](https://nodejs.org/)

### 1. Clone the repository
```sh
git clone https://github.com/eva672/auth_api2.git
cd auth_api2
```

### 2. Setup Environment Variables
Create a `.env` file in the root with:
```env
JWT_SALT=your_base64_16byte_salt
JWT_SECRET=your_jwt_secret
JWT_EXPIRATION=86400
```
- Generate a 16-byte salt and encode it in base64 (e.g., `openssl rand -base64 16`)

### 3. Run the Backend
```sh
cargo run
```
- The backend will start on `http://localhost:3000`

### 4. Run the Frontend
```sh
cd front-end
npm install
npm start
```
- The frontend will start on `http://localhost:3000` or `http://localhost:3001`

---

## 📖 API Documentation
- Swagger UI available at `/swagger-ui` when backend is running.

---

## 🖥️ Screenshots
> ![Login UI](./screenshots/login.png)
> ![Profile UI](./screenshots/profile.png)

---

## 🤝 Contributing
1. Fork the repo
2. Create your feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## 📄 License
This project is licensed under the MIT License.

---

## 🙏 Acknowledgements
- [Rust](https://www.rust-lang.org/)
- [Axum](https://github.com/tokio-rs/axum)
- [React](https://react.dev/)
- [Utoipa](https://github.com/juhaku/utoipa)

---

> Made with ❤️ by eva672
