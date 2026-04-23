# 🚀 PLM Agentic AI System (Predictive Maintenance)

A modular **multi-agent AI system** that simulates Product Lifecycle Management (PLM) using predictive maintenance principles.
The system ingests sensor data, evaluates equipment health, and autonomously generates maintenance decisions in real time.

---

## 🧠 Overview

Modern industrial systems require **proactive maintenance** to reduce downtime and operational risk.
This project demonstrates how **Agentic AI-inspired pipelines** can be applied to PLM workflows by decomposing the problem into specialized agents.

Each stage of the pipeline is handled by an independent module:

* 🔍 **Monitoring Agent** → Detects anomalies in sensor signals
* 📊 **Analytics Agent** → Estimates Remaining Useful Life (RUL) and failure probability
* 🧮 **Decision Agent** → Recommends maintenance actions based on risk thresholds

The system is exposed via a **FastAPI backend** and visualized using a **Streamlit dashboard**.

---

## ⚙️ Key Features

* 🔹 Modular multi-agent architecture
* 🔹 Real-time predictive maintenance simulation
* 🔹 RESTful API using FastAPI
* 🔹 Interactive dashboard using Streamlit
* 🔹 Structured JSON outputs for integration
* 🔹 Easily extensible for ML and real-world data

---

## 🏗️ System Architecture

```text
Sensor Data → Monitoring Agent → Analytics Agent → Decision Agent → Output
```

| Component  | Responsibility                              |
| ---------- | ------------------------------------------- |
| Monitoring | Detect anomalies in temperature & vibration |
| Analytics  | Estimate RUL and failure probability        |
| Decision   | Generate maintenance strategy               |

---

## 🧪 Sample Input

```json
{
  "temperature": 85,
  "vibration": 4.5,
  "cycle": 500
}
```

---

## 📤 Sample Output

```json
{
  "prediction": "IMMEDIATE MAINTENANCE",
  "context": {
    "monitoring": {"anomaly": true, "severity": "HIGH"},
    "analytics": {"rul": 500, "failure_prob_7d": 0.8},
    "decision": "IMMEDIATE MAINTENANCE"
  }
}
```

---

## 🚀 Getting Started

### 1. Clone Repository

```bash
git clone https://github.com/yourusername/plm-agentic-ai.git
cd plm-agentic-ai
```

---

### 2. Setup Virtual Environment

```bash
python -m venv .venv
.venv\Scripts\activate   # Windows
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Run Backend

```bash
uvicorn backend.main:app --reload
```

API available at:

```
http://127.0.0.1:8000/docs
```

---

### 5. Run Frontend

```bash
streamlit run ui/app.py
```

---

## 📡 API Reference

### POST `/predict`

**Request:**

```json
{
  "temperature": 85,
  "vibration": 4.5,
  "cycle": 500
}
```

**Response:**

```json
{
  "prediction": "...",
  "context": {...}
}
```

---

## 🧠 Technical Stack

* **Backend:** FastAPI
* **Frontend:** Streamlit
* **Language:** Python
* **Data Processing:** NumPy, Pandas

---

## 📊 Design Highlights

* ✔ Modular pipeline simulating agent-based workflows
* ✔ Decoupled components for scalability
* ✔ Interpretable decision logic
* ✔ API-first architecture

---

## ⚠️ Limitations

* Simulated sensor data (no real IoT integration)
* Simplified predictive model (rule + heuristic based)
* No persistent storage layer

---

## 🔮 Future Enhancements

* Integrate ML models (Isolation Forest, LSTM)
* Add real-time streaming (Kafka / MQTT)
* Deploy on cloud (AWS / Azure)
* Add logging, monitoring, and alerting
* Extend to full PLM lifecycle (design → production → maintenance)

---

## 👨‍💻 Author

**Rahul Prudhvi**

---

## ⭐ Support

If you found this useful, consider giving it a ⭐ on GitHub!
