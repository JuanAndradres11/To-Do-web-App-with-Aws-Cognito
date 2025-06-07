# To-Do-web-App-with-Aws-Cognito-and-RDS

# 📝 TODO Web App with AWS Cognito & RDS

A secure, full-stack TODO web application that uses **AWS Cognito** for user authentication and **AWS RDS** for persistent data storage. Users can register, log in, and manage personal task lists with full CRUD (Create, Read, Update, Delete) support.

---

## 🔧 Features

* 🔐 **User Authentication** via AWS Cognito (OAuth 2.0 / JWT-based)
* 🗄️ **Relational Database** powered by AWS RDS (e.g., PostgreSQL/MySQL)
* 🧾 Task management (Add, Edit, Delete, Mark as Done)

---

## 🛠️ Tech Stack

| Layer    | Technology           |
| -------- | -------------------- |
| Frontend | HTML/CSS/JS          |
| Backend  | Flask                |
| Auth     | AWS Cognito          |
| Database | AWS RDS (PostgreSQL) |
| Hosting  | Localhost            |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/aws-cognito-todo-app.git
cd aws-cognito-todo-app
```

### 2. Set Up Environment Variables

Create a `.env` file and define the following:

```env
COGNITO_USER_POOL_ID=your_user_pool_id
COGNITO_CLIENT_ID=your_client_id
COGNITO_REGION=your_aws_region
DATABASE_URL=postgresql://username:password@hostname/dbname
JWT_SECRET=your_jwt_verification_secret
```

> ⚠️ Never commit `.env` files.

---

### 3. Install Dependencies

**Python (Flask example)**

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

---

### 4. Run the Server

```bash
flask run
```

Navigate to `http://localhost:5000`

---

## 📦 API Endpoints (Example)

| Method | Endpoint      | Description         |
| ------ | ------------- | ------------------- |
| POST   | `/register`   | Register new user   |
| POST   | `/login`      | Login and get token |
| GET    | `/todos`      | Get user’s todos    |
| POST   | `/todos`      | Add a new todo      |
| PUT    | `/todos/<id>` | Update a todo       |
| DELETE | `/todos/<id>` | Delete a todo       |

---

## 🔒 Security Notes

* All endpoints are protected via Cognito-issued JWTs.
* Passwords are never stored — handled entirely by AWS Cognito.


## 🧰 Future Improvements

* ✅ Add password reset via Cognito
* 📲 Add mobile-responsive UI
* 🔁 Paginate long TODO lists
* 📊 Add task analytics dashboard

---

## 📄 License

MIT License. Feel free to fork, hack, and improve.


