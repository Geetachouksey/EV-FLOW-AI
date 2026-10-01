# EV-FLOW-AI
Multi-Agent AI system for intelligent EV fleet energy optimization and adaptive charging decisions.
# ⚡ EV-FLOW AI

### Multi-Agent AI System for EV Fleet Energy Optimization

EV-FLOW AI is an intelligent **multi-agent EV fleet energy optimization system** that helps make smart charging decisions based on battery status, vehicle priority, trip urgency, electricity prices, and charger availability.

The system uses multiple specialized AI agents and an orchestration layer to analyze EV fleet conditions and generate an appropriate charging strategy.

---

## 🚗 Problem Statement

Managing multiple Electric Vehicles (EVs) requires continuous decisions about:

- 🔋 Battery State of Charge (SOC)
- 🚗 Vehicle priority
- 🗺️ Trip urgency
- 🔌 Charger availability
- 💰 Electricity prices
- ⚠️ Charger failures
- 🚨 Emergency trips

A fixed charging schedule may not perform well when fleet conditions change.

**EV-FLOW AI addresses this challenge by coordinating multiple specialized agents to dynamically analyze fleet conditions and generate charging decisions.**

---

## 💡 Proposed Solution

EV-FLOW AI follows a **Multi-Agent AI Architecture**.

Each agent focuses on a specific part of the EV charging problem:

### 🔋 Battery Agent
Analyzes battery-related information such as:

- State of Charge (SOC)
- Battery readiness
- Critical battery conditions

### 🗺️ Route Agent
Analyzes:

- Trip urgency
- Vehicle requirements
- Emergency travel conditions

### 💰 Price Agent
Considers:

- Electricity price changes
- Cost-aware charging
- Peak and lower-cost charging periods

### ⚙️ Optimization Agent
Combines available information and generates an optimized charging strategy.

### 🧠 Decision Agent
Coordinates the agent outputs and produces the final decision.

---

## 🔄 AI Workflow

```text
                EV Fleet Data
                     │
                     ▼
             EV-FLOW AI Orchestrator
                     │
        ┌────────────┼────────────┐
        ▼            ▼            ▼
   🔋 Battery    🗺️ Route      💰 Price
      Agent        Agent         Agent
        │            │            │
        └────────────┼────────────┘
                     ▼
             ⚙️ Optimization Agent
                     │
                     ▼
              🧠 Decision Agent
                     │
                     ▼
             🚗 Charging Decision
```

---

## 🖥️ Interactive Dashboard

The project includes an interactive dashboard built using Python and `ipywidgets`.

The dashboard displays important fleet-level information including:

- 🚗 Total EVs
- 🔴 Critical battery vehicles
- 🟠 High-priority vehicles
- 🔌 Available chargers

It also provides a visual representation of the AI agent network and the current fleet charging plan.

---

## 🔄 What-If AI Simulator

EV-FLOW AI includes a scenario-based simulator that demonstrates how the system can respond to changing fleet conditions.

### 🟢 Normal Operation

The system maintains the existing fleet charging plan.

```text
System Status → NORMAL

Decision:
Maintain current charging schedule.
```

### 🔴 CH02 Charger Failure

The system detects the failure of charger CH02 and evaluates the remaining charging capacity.

```text
CH02 Failure
     ↓
Charger Availability Analysis
     ↓
Charging Load Reallocation
     ↓
Critical EVs Prioritized
```

### 🟠 Electricity Price +40%

The Price Agent detects an electricity price increase.

The optimization strategy focuses on:

- Prioritizing urgent EVs
- Shifting flexible charging to lower-cost periods
- Avoiding unnecessary peak-price charging

### 🚨 EV01 Emergency Trip

When EV01 requires an emergency trip:

```text
Route Agent
     ↓
EV01 marked URGENT
     ↓
Battery Readiness Check
     ↓
Optimization Agent
     ↓
EV01 receives highest priority
     ↓
CHARGE EV01 IMMEDIATELY
```

---

## 🧠 Agent Orchestration

The EV-FLOW AI orchestrator processes vehicle information and coordinates different agent outputs.

Example:

```python
vehicle = vehicles.iloc[0]

orchestrator_result = ev_flow_orchestrator(vehicle)
```

The system can then display the individual agent results:

```python
print(orchestrator_result["battery"])
print(orchestrator_result["route"])
print(orchestrator_result["price"])
print(orchestrator_result["final"])
```

This makes the decision-making process easier to understand and demonstrate.

---

## 🎯 Key Features

- ✅ Multi-Agent AI architecture
- ✅ Battery-aware decision making
- ✅ Vehicle priority management
- ✅ Trip urgency analysis
- ✅ Electricity price awareness
- ✅ Charger failure handling
- ✅ Emergency EV prioritization
- ✅ Dynamic charging strategy
- ✅ Interactive dashboard
- ✅ What-If scenario simulator
- ✅ Fleet charging plan visualization
- ✅ AI decision orchestration

---

## 🛠️ Technology Stack

### Programming

- Python
- Pandas
- NumPy

### AI & Decision System

- Multi-Agent AI Architecture
- Agent Orchestration
- Rule-based scenario simulation

### Interactive Interface

- IPyWidgets
- IPython Display
- HTML-based dashboard rendering

### Development Environment

- Jupyter Notebook
- Google Colab / Python Environment
- VS Code

---

## 📊 Example Scenarios

The simulator supports the following scenarios:

| Scenario | System Response |
|---|---|
| 🟢 Normal Operation | Maintain current charging plan |
| 🔴 CH02 Charger Failure | Reallocate charging capacity |
| 🟠 Electricity Price +40% | Generate cost-aware charging strategy |
| 🚨 EV01 Emergency Trip | Give EV01 highest charging priority |

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/EV-FLOW-AI.git
```

Open the project:

```bash
cd EV-FLOW-AI
```

Install dependencies:

```bash
pip install pandas numpy ipywidgets jupyter
```

Start Jupyter:

```bash
jupyter notebook
```

Open the project notebook or Python file and run the required cells/files.

---

## ▶️ How to Run

1. Install the required Python libraries.
2. Load the EV and charger datasets.
3. Initialize the EV fleet and charging data.
4. Run the AI agent functions.
5. Run the EV-FLOW orchestrator.
6. Open the interactive dashboard.
7. Select a scenario from the What-If Simulator.
8. Click **⚡ RUN AI SIMULATION**.
9. Observe how the system changes its charging strategy.

---

## 📁 Suggested Project Structure

```text
EV-FLOW-AI/
│
├── README.md
├── requirements.txt
│
├── src/
│   ├── agents.py
│   ├── orchestrator.py
│   ├── simulator.py
│   └── dashboard.py
│
├── data/
│   ├── vehicles.csv
│   └── chargers.csv
│
└── screenshots/
    └── dashboard.png
```

> The exact file structure can be adjusted according to the implementation in the repository.

---

## 🔮 Future Scope

EV-FLOW AI can be extended into a real-world EV fleet management platform.

Future improvements may include:

- 📡 Real-time EV and charger monitoring
- 🔌 Live charger integration
- 💰 Real-time electricity tariff APIs
- 🗺️ Live route and traffic data
- 🔋 Predictive battery analytics
- 🤖 Advanced autonomous charging optimization
- ☁️ Cloud-based fleet management
- 📱 Mobile application
- 🌱 Renewable-energy-aware charging
- 📊 Advanced fleet analytics
- 🔐 Secure fleet and user authentication

---

## 🌱 Potential Applications

EV-FLOW AI can be adapted for:

- Corporate EV fleets
- Delivery and logistics fleets
- EV charging stations
- Smart campuses
- Commercial EV depots
- Fleet management systems
- Smart energy management

---

## 🏆 Project Concept

EV-FLOW AI follows a simple intelligent decision cycle:

```text
SENSE
  ↓
ANALYZE
  ↓
COORDINATE
  ↓
OPTIMIZE
  ↓
DECIDE
```

The goal is to demonstrate how **multi-agent AI can coordinate different EV-related factors and dynamically respond to changing fleet conditions.**

---

## 👩‍💻 Author

**Geeta Chouksey**

B.Tech — Industrial Internet of Things (IIoT)

### Interests

- Artificial Intelligence
- IoT
- Multi-Agent Systems
- Smart Energy Systems
- Electric Vehicles
- Automation

---

## 📜 License

This project is developed for **educational, research, and prototype purposes**.

---

# ⚡ EV-FLOW AI

### Intelligent Decisions. Smarter Charging. Better EV Fleet Management. 🚗🔋
