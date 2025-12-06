# ThreatGradient

**AI-Driven Adversary Intelligence Platform**\
*Comprising **GradientSim** (AI Adversary Emulation) and
**GradientPhantom** (AI Detection & Narrative Engine).*

ThreatGradient is an innovative security research project that unifies
**AI-generated adversary simulation** with **AI-assisted detection
analytics**.\
It models how attackers *might* move through an environment
(GradientSim) and explains how attackers *did* move through logs
(GradientPhantom).

This project demonstrates expertise in: - adversary emulation\
- detection engineering\
- ML-driven anomaly scoring\
- MITRE ATT&CK mapping\
- AI security research\
- log correlation + behavioral reasoning

------------------------------------------------------------------------

## 🚀 Platform Overview

### **ThreatGradient**

The umbrella platform that orchestrates both engines.\
It provides: - a unified UI\
- a shared MITRE ATT&CK knowledge graph\
- vector embeddings for behavior and TTP similarity\
- reporting, export, and visualization layers

ThreatGradient's goal:\
\> **Predict attacker behavior, observe real attacker traces, and unify
both into one continuous intelligence cycle.**

------------------------------------------------------------------------

# 🧠 Core Modules

------------------------------------------------------------------------

## 1. GradientSim --- *AI Adversary Emulation Engine*

*"Model an APT campaign before it happens."*

GradientSim analyzes: - network diagrams\
- asset inventories\
- trust boundaries\
- open ports / exposed services\
- privilege relationships

It then: - generates possible attack paths\
- constructs multi-step adversary campaigns\
- maps each phase to MITRE ATT&CK\
- highlights choke points, weakest links, and blast radius\
- exports the simulated campaign as a graph, heatmap, or narrative

**Input Examples** - JSON network model\
- Diagram text description\
- Parsed cloud asset inventory\
- Manual topology description

**Output Examples** - Attack graph (D3.js)\
- MITRE heatmap\
- AI-generated "Attacker Playbook"\
- Risk scoring per path\
- Recommended detections / enrichments

------------------------------------------------------------------------

## 2. GradientPhantom --- *AI Detection & Narrative Engine*

*"See the attacker inside your logs."*

GradientPhantom ingests: - Sysmon logs\
- Windows Event Logs\
- Linux audit logs\
- Process telemetry\
- Command lines\
- Registry operations\
- File modifications\
- Authentication events

It performs: - ML anomaly scoring\
- behavioral clustering\
- detection of multi-event attack chains\
- MITRE ATT&CK mapping\
- timeline reconstruction

Then it generates: - an "attacker storyline"\
- possible intent + objective (in plain language)\
- a heatmap of touched TTPs\
- confidence scoring

**Output Example**

    [GradientPhantom Narrative]

    The host displayed signs consistent with credential access (T1003).
    Sequence:
    1. Suspicious LSASS read attempt
    2. Unusual PowerShell host execution
    3. Registry modification consistent with persistence
    Overall likelihood of compromise: High (0.89)

------------------------------------------------------------------------

# 🔄 The ThreatGradient Intelligence Loop

ThreatGradient enables a continuous cycle:

1.  **Predict** --- GradientSim forecasts viable attacker routes\
2.  **Observe** --- GradientPhantom reconstructs real attacker
    behaviors\
3.  **Refine** --- Detection logic and simulation paths improve each
    other

------------------------------------------------------------------------

# 🧱 Architecture (High-Level)

    ThreatGradient Platform
    │
    ├── GradientSim
    │   ├── Topology Parser
    │   ├── Attack Path Engine
    │   ├── MITRE Mapping Engine
    │   ├── Risk Scoring Model
    │   └── Simulation Visualizer (D3.js)
    │
    └── GradientPhantom
        ├── Log Ingestion Layer
        ├── Feature Extraction & Embedding
        ├── ML Anomaly Scoring
        ├── Behavior Chain Correlator
        ├── Timeline + Narrative Generator
        └── Detection Heatmap Renderer

------------------------------------------------------------------------

# 🛠️ Tech Stack (Planned)

  Layer            Tech
  ---------------- -------------------------
  UI               React, Tailwind, Vite
  Visualizations   D3.js, Mermaid
  Backend          Python (FastAPI)
  AI Models        PyTorch + embeddings
  Data             SQLite/Postgres
  Optional         Neo4j for attack graphs

------------------------------------------------------------------------

# 📂 Repository Structure (Proposed)

    /threatgradient
    │
    ├── /gradientsim
    │   ├── parsers/
    │   ├── models/
    │   ├── mitre/
    │   ├── visualization/
    │   └── examples/
    │
    ├── /gradientphantom
    │   ├── ingest/
    │   ├── detection/
    │   ├── embeddings/
    │   ├── narratives/
    │   └── samples/
    │
    ├── /shared
    │   ├── mitre_graph/
    │   ├── utils/
    │   └── schema/
    │
    └── /ui
        ├── components/
        ├── pages/
        └── visualizations/

------------------------------------------------------------------------

# 📈 Roadmap

### **Stage 1 --- MVP**

-   Parse simple topologies\
-   Basic attack path generation\
-   Sysmon ingestion + baseline anomaly scoring\
-   JSON/HTML reporting

### **Stage 2 --- AI Reasoning**

-   Full narrative generator\
-   Embedding-based TTP similarity model\
-   MITRE heatmap generation

### **Stage 3 --- UI Platform**

-   React interface\
-   Attack graph explorer\
-   Detection storyline viewer

### **Stage 4 --- Intelligence Loop**

-   Automatically improve detection from simulation\
-   Feedback system between modules

------------------------------------------------------------------------

# 📜 License

MIT License

------------------------------------------------------------------------

# 🤝 Contributions

Open to PRs for: - MITRE mapping improvements\
- log parsing modules\
- new attack simulation models
