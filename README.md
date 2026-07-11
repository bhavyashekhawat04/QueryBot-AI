# QueryBot-AI

An AI-powered query assistant built with **Python**, **Streamlit**, **Google's Generative AI SDK**, **PostgreSQL (AWS RDS)**, and **Docker**. The application generates AI responses and stores every user query and generated response in a PostgreSQL database.

---

## 🚀 Features

- 🤖 AI-powered query assistant
- 💬 Interactive web interface built with Streamlit
- 🗄️ Stores user queries and AI responses in PostgreSQL
- ☁️ Supports AWS RDS for cloud database hosting
- 🐳 Docker support for containerized deployment
- 🔐 Secure configuration using environment variables
- 📊 Automatically creates the required database table if it doesn't exist

---

## 🛠️ Tech Stack

- Python
- Streamlit
- Google Generative AI SDK
- PostgreSQL
- AWS RDS
- Docker
- psycopg2
- python-dotenv

---

## 📁 Project Structure

```text
QueryBot-AI/
├── app.py
├── Dockerfile
├── pyproject.toml
├── requirements.txt
├── uv.lock
├── .env.example
├── .gitignore
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/QueryBot-AI.git
cd QueryBot-AI
```

### 2. Install dependencies

Using pip:

```bash
pip install -r requirements.txt
```

Or using uv:

```bash
uv sync
```

---

## 🔑 Environment Variables

Create a `.env` file in the project root.

```env
GOOGLE_API_KEY=YOUR_GOOGLE_API_KEY

DB_HOST=YOUR_DATABASE_HOST
DB_NAME=YOUR_DATABASE_NAME
DB_USER=YOUR_DATABASE_USERNAME
DB_PASSWORD=YOUR_DATABASE_PASSWORD
DB_PORT=5432
```

---

## ▶️ Run the Application

```bash
streamlit run app.py
```

The application will be available at:

```text
http://localhost:8501
```

---

## 🗄️ Database

The application automatically creates the following table if it does not already exist:

| Column | Type |
|---------|------|
| id | SERIAL |
| user_input | TEXT |
| bot_response | TEXT |

Each user query and AI-generated response is stored in the database for future reference.

---

## 🐳 Run with Docker

Build the Docker image:

```bash
docker build -t querybot-ai .
```

Run the container:

```bash
docker run -p 8501:8501 querybot-ai
```

---

## 📌 Future Improvements

- Chat history page
- Authentication and user accounts
- Multiple AI model support
- Conversation memory
- Export chat history
- Cloud deployment automation
- REST API integration

---

## 👨‍💻 Author

**Bhavya Shekhawat**

---

## ⭐ If you found this project helpful, consider giving it a star!
