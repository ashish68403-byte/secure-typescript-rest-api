# 🚀 TypeScript REST API

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white)

A production-ready **RESTful CRUD API** built with **TypeScript**, featuring JWT authentication, structured routing, and a clean MVC architecture — part of the MERN stack.

</div>

---

## 📁 Project Structure

```
typescript-rest-api/
├── src/
│   ├── controllers/
│   │   ├── authentication.ts    # Auth logic (register, login)
│   │   └── users.ts             # User CRUD operations
│   ├── db/
│   │   └── users.ts             # Database models & queries
│   ├── helpers/
│   │   └── index.ts             # Utility/helper functions
│   ├── middlewares/
│   │   └── index.ts             # Auth & validation middlewares
│   ├── router/
│   │   ├── authentication.ts    # Auth routes
│   │   ├── users.ts             # User routes
│   │   └── index.ts             # Route aggregator
│   └── index.ts                 # App entry point
├── .gitignore
├── nodemon.json
├── package.json
├── package-lock.json
└── tsconfig.json
```

---

## ✨ Features

- ✅ **Full CRUD** operations for user management
- ✅ **JWT Authentication** — secure token-based auth
- ✅ **TypeScript** — fully typed for reliability and scalability
- ✅ **MVC Architecture** — clean separation of concerns
- ✅ **MongoDB** — NoSQL database integration
- ✅ **Custom Middleware** — authentication guards on protected routes
- ✅ **Nodemon** — hot-reloading for development

---

## 🛠️ Tech Stack

| Layer        | Technology              |
|--------------|-------------------------|
| Language     | TypeScript              |
| Runtime      | Node.js                 |
| Framework    | Express.js              |
| Database     | MongoDB                 |
| Auth         | JSON Web Tokens (JWT)   |
| Dev Tool     | Nodemon                 |

---

## ⚙️ Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v18 or above)
- [MongoDB](https://www.mongodb.com/) (local or Atlas)
- npm or yarn

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/ashish68403-byte/typescript-rest-api.git
cd typescript-rest-api
```

2. **Install dependencies**

```bash
npm install
```

3. **Set up environment variables**

Create a `.env` file in the root directory:

```env
PORT=8080
MONGO_URL=your_mongodb_connection_string
SECRET=your_jwt_secret_key
```

4. **Run the development server**

```bash
npm run dev
```

The server will start at `http://localhost:8080`

---

## 📡 API Endpoints

### 🔐 Authentication

| Method | Endpoint              | Description         | Access  |
|--------|-----------------------|---------------------|---------|
| POST   | `/auth/register`      | Register a new user | Public  |
| POST   | `/auth/login`         | Login & get token   | Public  |

### 👤 Users

| Method | Endpoint              | Description            | Access    |
|--------|-----------------------|------------------------|-----------|
| GET    | `/users`              | Get all users          | Protected |
| GET    | `/users/:id`          | Get user by ID         | Protected |
| PUT    | `/users/:id`          | Update user by ID      | Protected |
| DELETE | `/users/:id`          | Delete user by ID      | Protected |

> 🔒 **Protected routes** require a valid JWT token in the `Authorization` header:
> ```
> Authorization: Bearer <your_token>
> ```

---

## 🧪 Example Request

### Register a User

```http
POST /auth/register
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "securepassword123",
  "username": "johndoe"
}
```

### Login

```http
POST /auth/login
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "securepassword123"
}
```

**Response:**
```json
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}
```

---

## 📜 Scripts

| Script          | Command           | Description                  |
|-----------------|-------------------|------------------------------|
| Development     | `npm run dev`     | Start with hot-reloading      |
| Build           | `npm run build`   | Compile TypeScript to JS      |
| Start           | `npm start`       | Run compiled production build |

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 👨‍💻 Author

**Ashish** — [@ashish68403-byte](https://github.com/ashish68403-byte)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<div align="center">
  Made with ❤️ and TypeScript
</div>
