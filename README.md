# 🚀 DecodeLabs Project 3 - Database Integration API

A full-stack backend project demonstrating **Database Integration, CRUD Operations, RESTful APIs, Validation, and MongoDB Connectivity** using Node.js, Express.js, and Mongoose.

This project follows a structured architecture based on four core software development pillars:

- 🏗️ Blueprint (Schema Design)
- 🌉 Bridge (Database Integration)
- ⚡ Action (CRUD Operations)
- 🛡️ Shield (Validation & Security)

---

## 📌 Features

### ✅ MongoDB Database Integration
- MongoDB Atlas / Local MongoDB Support
- Mongoose ODM
- Environment-based configuration

### ✅ Complete CRUD Operations
- Create User
- Read All Users
- Read User By ID
- Update User
- Partial Update User
- Delete User

### ✅ Data Validation
- Email format validation
- Age restrictions
- Required fields validation
- Role-based validation
- Duplicate email prevention

### ✅ Advanced Query Features
- Search users by name/email
- Filter users by role
- Pagination support
- Sorting support

### ✅ Error Handling
- Global error handler
- Custom 404 responses
- Validation error messages
- Invalid ObjectId handling

---

# 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Node.js | Runtime Environment |
| Express.js | Backend Framework |
| MongoDB | Database |
| Mongoose | ODM |
| Express Validator | Input Validation |
| Dotenv | Environment Variables |
| CORS | Cross-Origin Requests |

---

# 📂 Project Structure

```bash
decodelabs-p3/
│
├── config/
│   └── db.js
│
├── models/
│   └── User.js
│
├── routes/
│   └── users.js
│
├── .env.example
├── .gitignore
├── package.json
└── server.js
```

---

# 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/your-username/decodelabs-p3-database-integration.git
```

Move to the project folder:

```bash
cd decodelabs-p3
```

Install dependencies:

```bash
npm install
```

---

# ⚙️ Environment Setup

Create a `.env` file:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
```

Example:

```env
MONGO_URI=mongodb://localhost:27017/decodelabs_p3
```

or

```env
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/decodelabs_p3
```

---

# ▶️ Running the Application

Development Mode:

```bash
npm run dev
```

Production Mode:

```bash
npm start
```

Server URL:

```bash
http://localhost:5000
```

---

# 📖 API Endpoints

## Create User

```http
POST /api/users
```

Request Body:

```json
{
  "name": "Sonakshi Sharma",
  "email": "sona@example.com",
  "age": 21,
  "role": "student"
}
```

---

## Get All Users

```http
GET /api/users
```

Supports:

```http
/api/users?page=1&limit=10
/api/users?role=student
/api/users?search=sona
```

---

## Get User By ID

```http
GET /api/users/:id
```

---

## Update User

```http
PUT /api/users/:id
```

---

## Partial Update User

```http
PATCH /api/users/:id
```

---

## Delete User

```http
DELETE /api/users/:id
```

---

# 🗄️ Database Schema

```javascript
{
  name: String,
  email: String,
  age: Number,
  role: String,
  isActive: Boolean
}
```

### Validation Rules

| Field | Validation |
|---------|------------|
| Name | Required, 2-50 chars |
| Email | Required, Unique |
| Age | Minimum 18 |
| Role | student, instructor, admin |

---

# 📊 Sample Response

```json
{
  "success": true,
  "message": "User created successfully",
  "data": {
    "_id": "123abc",
    "name": "Sonakshi Sharma",
    "email": "sona@example.com",
    "age": 21,
    "role": "student"
  }
}
```

---

# 🔒 Security Features

- Input Validation
- Duplicate Email Protection
- Error Handling Middleware
- Environment Variable Protection
- MongoDB Injection Prevention
- Route Protection Architecture

---

# 🎯 Learning Outcomes

Through this project, I learned:

- REST API Development
- MongoDB Integration
- Mongoose Schema Design
- CRUD Operations
- API Validation
- Backend Architecture
- Error Handling
- Environment Configuration

---

# 🔮 Future Enhancements

- JWT Authentication
- Password Encryption
- Role-Based Authorization
- User Login System
- Swagger Documentation
- Docker Deployment
- Unit Testing

---

# 👩‍💻 Author

**Sonakshi Sharma**

B.Tech Computer Science Engineering  
Aspiring Full Stack Developer | Backend Enthusiast

---

# ⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub.
