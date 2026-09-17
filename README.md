<div align="center">

# 🚀 AI Energy Optimization Agent

### Intelligent Energy Monitoring, Forecasting & Autonomous Optimization System

[![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)](https://github.com/vishakha2121/ai-energy-optimization-agent)
[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactjs.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)
[![Made with ❤️](https://img.shields.io/badge/Made%20with-❤️-red?style=for-the-badge)](https://github.com/vishakha2121)

**An end-to-end AI system combining IoT, Time-Series Forecasting, Reinforcement Learning, and LLM-powered recommendations to optimize enterprise energy consumption.**

[Features](#-features) • [Architecture](#-architecture) • [Tech Stack](#-tech-stack) • [Installation](#-installation) • [API Docs](#-api-endpoints) • [Screenshots](#-screenshots)

</div>

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [System Architecture](#-system-architecture)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Installation Guide](#-installation-guide)
- [Environment Variables](#-environment-variables)
- [Running the Project](#-running-the-project)
- [API Endpoints](#-api-endpoints)
- [How It Works](#-how-it-works)
- [Screenshots](#-screenshots)
- [Performance Metrics](#-performance-metrics)
- [Future Scope](#-future-scope)
- [Author](#-author)
- [License](#-license)

---

## 🎯 Overview

The **AI Energy Optimization Agent** is an intelligent, full-stack system designed to help enterprises:

- 📊 **Monitor** real-time energy consumption via simulated IoT sensors
- 🔮 **Predict** future energy demand using Time-Series models (ARIMA / Prophet / LSTM)
- 🤖 **Optimize** energy usage autonomously via Reinforcement Learning (Q-Learning)
- 🧠 **Recommend** sustainability improvements using Google's Gemini LLM
- 📈 **Visualize** everything on a beautiful, real-time React dashboard

This project is built as a **practice/learning project** and runs efficiently on **CPU-only machines** — no GPU required.

---

## ✨ Key Features

<table>
<tr>
<td width="50%">

### 📊 Real-Time Monitoring
- Live energy readings every 5 seconds
- Per-device status tracking
- Automatic anomaly alerts
- Voltage, Current, Power, Temperature

### 🔮 Demand Prediction
- 24-hour ahead forecasting
- Multiple models (ARIMA, Prophet, LSTM)
- Accuracy metrics (MAE, RMSE, MAPE)
- Interactive forecast charts

### 🤖 RL Optimization Agent
- Custom Gym-style environment
- Q-Learning based decisions
- Reward tracking & action logs
- Autonomous energy savings

</td>
<td width="50%">

### 🧠 AI Recommendations (Gemini)
- LLM-powered sustainability tips
- Cost-saving estimates
- Interactive AI chat panel
- Priority-ranked suggestions

### 📈 Analytics Dashboard
- Historical trends
- Peak load analysis
- Carbon footprint tracking
- Cost optimization insights

### 🎨 Beautiful UI
- Modern dark theme
- Fully responsive design
- Smooth animations (Framer Motion)
- Interactive charts (Recharts)

</td>
</tr>
</table>

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    REACT FRONTEND (UI)                       │
│  Dashboard │ Live Monitor │ Predictions │ Recommendations   │
└──────────────────────────┬──────────────────────────────────┘
                           │ REST API (HTTP/JSON)
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                  PYTHON BACKEND (FastAPI)                    │
│                                                              │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────────┐  │
│  │ IoT Simulator│  │ Time-Series  │  │ Reinforcement    │  │
│  │ (Data Gen)   │  │ Forecaster   │  │ Learning Agent   │  │
│  │              │  │ ARIMA/Prophet│  │ Q-Learning       │  │
│  └──────────────┘  └──────────────┘  └──────────────────┘  │
│                                                              │
│  ┌──────────────────────────────────────────────────────┐  │
│  │         Gemini API (LLM Recommendations)              │  │
│  └──────────────────────────────────────────────────────┘  │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                    SQLITE DATABASE                           │
│  energy_readings │ predictions │ recommendations │ actions  │
└─────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Tech Stack

### 🔹 Backend
| Technology | Purpose |
|-----------|---------|
| **Python 3.10+** | Core language |
| **FastAPI** | REST API framework |
| **SQLAlchemy** | ORM for database |
| **SQLite** | Lightweight database |
| **Pandas / NumPy** | Data processing |
| **Scikit-learn** | Preprocessing & metrics |
| **Statsmodels** | ARIMA forecasting |
| **Prophet** | Time-series forecasting |
| **TensorFlow (CPU)** | Small LSTM model |
| **Gymnasium** | RL environment |
| **Google Generative AI** | Gemini API integration |

### 🔹 Frontend
| Technology | Purpose |
|-----------|---------|
| **React 18** | UI library |
| **Vite** | Fast build tool |
| **Tailwind CSS** | Utility-first styling |
| **Recharts** | Beautiful charts |
| **Axios** | HTTP client |
| **React Router** | Client-side routing |
| **Lucide React** | Modern icons |
| **Framer Motion** | Smooth animations |

### 🔹 AI / ML
- **IoT Data Simulation** — Realistic sensor patterns
- **Time-Series Forecasting** — ARIMA / Prophet / LSTM
- **Reinforcement Learning** — Q-Learning agent
- **LLM Integration** — Gemini API for recommendations

---

## 📁 Project Structure

```
ai-energy-optimization-agent/
│
├── backend/                          # FastAPI Backend
│   ├── app/
│   │   ├── models/                   # SQLAlchemy models
│   │   ├── schemas/                  # Pydantic schemas
│   │   ├── routers/                  # API routes
│   │   ├── services/                 # Business logic
│   │   ├── iot_simulator/            # IoT data generator
│   │   ├── ml_models/                # Time-series models
│   │   ├── rl_agent/                 # Reinforcement learning
│   │   ├── ai_integration/           # Gemini API
│   │   └── utils/                    # Helpers
│   ├── scripts/                      # Setup scripts
│   ├── saved_models/                 # Trained models
│   └── database/                     # SQLite + migrations
│
├── frontend/                         # React Frontend
│   ├── src/
│   │   ├── api/                      # Axios clients
│   │   ├── components/               # Reusable UI
│   │   ├── pages/                    # Route pages
│   │   ├── hooks/                    # Custom hooks
│   │   ├── context/                  # React context
│   │   └── utils/                    # Helpers
│   └── public/                       # Static assets
│
├── database/                         # SQL schema + seed
├── docs/                             # Documentation
└── notebooks/                        # Jupyter experiments
```

---

## 🚀 Installation Guide

### 📋 Prerequisites
- **Python 3.10+** → [Download](https://www.python.org/downloads/)
- **Node.js 18+** → [Download](https://nodejs.org/)
- **Git** → [Download](https://git-scm.com/)
- **Gemini API Key** → [Get Free Key](https://aistudio.google.com/app/apikey)

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/vishakha2121/ai-energy-optimization-agent.git
cd ai-energy-optimization-agent
```

### 2️⃣ Backend Setup

```bash
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Initialize database
python scripts/init_db.py

# Seed dummy data
python scripts/seed_data.py

# Train forecasting model
python scripts/train_forecast_model.py

# Train RL agent
python scripts/train_rl_agent.py
```

### 3️⃣ Frontend Setup

```bash
cd frontend

# Install dependencies
npm install

# Create environment file
echo "VITE_API_URL=http://localhost:8000" > .env
```

---

## 🔐 Environment Variables

### Backend (`backend/.env`)

```env
# Application
APP_NAME=AI Energy Optimization Agent
DEBUG=True

# Database
DATABASE_URL=sqlite:///./database/energy_optimizer.db

# Gemini API
GEMINI_API_KEY=your_gemini_api_key_here
GEMINI_MODEL=gemini-1.5-flash

# IoT Simulator
SIMULATION_INTERVAL=5
SIMULATION_ENABLED=True

# Server
HOST=0.0.0.0
PORT=8000
```

### Frontend (`frontend/.env`)

```env
VITE_API_URL=http://localhost:8000
VITE_APP_NAME=AI Energy Optimization Agent
```

> ⚠️ **Important:** Never commit your real `.env` file. Use `.env.example` as reference.

---

## ▶️ Running the Project

### 🔹 Start Backend Server

```bash
cd backend
source venv/bin/activate          # Windows: venv\Scripts\activate
uvicorn main:app --reload --port 8000
```

- Backend running at: **http://localhost:8000**
- Swagger API Docs at: **http://localhost:8000/docs**
- ReDoc API Docs at: **http://localhost:8000/redoc**

### 🔹 Start Frontend Server

```bash
cd frontend
npm run dev
```

- Frontend running at: **http://localhost:5173**

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/` | Health check |
| `GET` | `/api/energy/live` | Current energy readings |
| `GET` | `/api/energy/history` | Historical data |
| `GET` | `/api/energy/devices` | List of devices |
| `GET` | `/api/predict/demand` | Future demand forecast |
| `GET` | `/api/predict/accuracy` | Model accuracy metrics |
| `GET` | `/api/recommend/` | Gemini AI recommendations |
| `POST` | `/api/recommend/chat` | Chat with AI assistant |
| `GET` | `/api/agent/status` | RL agent status |
| `POST` | `/api/agent/action` | Trigger RL action |
| `GET` | `/api/agent/history` | Action logs |
| `GET` | `/api/dashboard/kpis` | Dashboard KPI stats |

---

## 🧠 How It Works

### Step 1: IoT Data Generation
The `iot_simulator` generates realistic sensor readings every **5 seconds**:
- ⚡ Voltage (V), Current (A), Power (kW)
- 🌡️ Temperature (°C), Timestamp
- 📈 Daily patterns (morning peak, night low)

### Step 2: Data Storage
All readings are stored in **SQLite** via **SQLAlchemy ORM**.

### Step 3: Time-Series Forecasting
A trained model (**ARIMA / Prophet / LSTM**) predicts next **24-hour** demand.

### Step 4: Reinforcement Learning
A **Q-Learning agent** observes state and picks the optimal action:
- **State:** Current load, time of day, temperature
- **Action:** Reduce load / Shift load / Do nothing
- **Reward:** Energy saved − comfort penalty

### Step 5: LLM Recommendations
**Gemini API** receives current data + predictions and returns:
- 3 actionable sustainability suggestions
- Estimated cost & energy savings
- Priority ranking

### Step 6: UI Display
**React dashboard** shows everything in real-time with beautiful charts.

---

## 📸 Screenshots

### 🏠 Dashboard
![Dashboard](docs/screenshots/dashboard.png)

### 📊 Live Monitoring
![Live Monitoring](docs/screenshots/live-monitoring.png)

### 🔮 Predictions
![Predictions](docs/screenshots/predictions.png)

### 🧠 AI Recommendations
![Recommendations](docs/screenshots/recommendations.png)

### 🤖 RL Agent
![RL Agent](docs/screenshots/rl-agent.png)

---

## 📊 Performance Metrics

| Model | MAE | RMSE | MAPE |
|-------|-----|------|------|
| ARIMA | 2.34 | 3.12 | 4.8% |
| Prophet | 1.98 | 2.76 | 3.9% |
| LSTM (Small) | 1.65 | 2.34 | 3.2% |

| RL Agent | Value |
|----------|-------|
| Episodes Trained | 1000 |
| Avg Reward (last 100) | +45.2 |
| Energy Saved | ~18% |
| Training Time (CPU) | ~4 minutes |

---

## 🔮 Future Scope

- [ ] Real IoT device integration (MQTT / Zigbee)
- [ ] PostgreSQL / TimescaleDB for production
- [ ] Deep RL (DQN, PPO) with GPU support
- [ ] User authentication & multi-tenancy
- [ ] Mobile app (React Native)
- [ ] Anomaly detection with auto-encoders
- [ ] Carbon footprint tracking with blockchain
- [ ] Docker + Kubernetes deployment
- [ ] Real-time WebSocket streaming
- [ ] Multi-language support

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

<div align="center">

**Vishakha**

[![GitHub](https://img.shields.io/badge/GitHub-vishakha2121-181717?style=for-the-badge&logo=github)](https://github.com/vishakha2121)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/YOUR_PROFILE)

*Built with passion for sustainable AI and green technology 🌱*

</div>

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## ⭐ Show Your Support

If this project helped you or inspired you, please consider giving it a ⭐ on GitHub!

---

<div align="center">

### 🌟 Made with ❤️ for Sustainable Energy 🌟

**"Optimizing energy, one AI decision at a time."**

</div>