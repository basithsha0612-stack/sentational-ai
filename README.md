# SENTINEL AI // Autonomous Network Intrusion Detection System (NIDS)

SENTINEL AI is a state-of-the-art, web-based Network Intrusion Detection System and Security Operations Center (SOC) dashboard. It implements the complete autonomous threat detection and incident response pipeline:

```text
User Login
    ↓
IDS Dashboard
    ↓
Upload / Enter Network Data
    ↓
AI/ML Analysis
    ↓
┌──────────────────────┐
│ Normal Traffic       │
│ OR                   │
│ Intrusion Detected   │
└──────────────────────┘
    ↓
Alert + Report
```

---

## Architecture & Workflow Stages

### 1. `User Login` (Security Clearance & Authentication)
- **SOC Clearance Gateway**: Role-based access control with clearance ratings (`TOP SECRET // SCI`, `DIRECTORATE // ALPHA`, `EXECUTIVE // OMNI`).
- **Quick Role Switcher**: One-click demo credentials for:
  - *Alex Mercer* (SOC Level 3 Analyst)
  - *Elena Rostova* (Senior Threat Hunter)
  - *Marcus Vance* (Chief Information Security Officer)
- **Hardware Token & Biometrics**: Simulated FIDO2 / YubiKey fingerprint laser scanner with audio-visual feedback.

### 2. `IDS Dashboard` (Live Telemetry & Perimeter Monitoring)
- **Live Oscilloscope Canvas**: Real-time 60fps HTML5 Canvas waveform rendering normal packet flows vs. anomalous intrusion bursts.
- **Key Performance Indicators (KPIs)**: Packets inspected counter, 98.37% normal traffic integrity, neutralized intrusions count, and real-time edge inference latency (1.42ms).
- **Attack Vector Distribution**: Radial breakdown across SYN Flood (DDoS), Port Scans, SQL Injection, SSH Brute Force, and C2 Botnet Beaconing.
- **Live Captured Flows Feed**: Telemetry feed with one-click "Inspect with AI" for every captured packet flow.

### 3. `Upload / Enter Network Data` (Ingestion Engine)
- **Mode A: Enter Network Data (Packet Crafter)**:
  - Comprehensive feature input: Source/Destination IP & Port, Protocol (TCP, UDP, ICMP, HTTP, DNS, SSH), Flow Duration, Packet Size, TCP Flags (SYN, ACK, RST, FIN, URG), Packet Flow Rate, and Failed Logins.
  - **Attack Preset Library**:
    - 🟢 *Normal HTTPS Web Browsing* (RFC 793 compliant)
    - 🔴 *DDoS SYN Flood* (Volumetric half-open exhaustion)
    - 🟠 *Nmap Stealth SYN Port Scan* (Network reconnaissance)
    - 🔴 *SSH / RDP Brute Force* (Authentication spray)
    - 🟣 *SQL Injection & Data Exfiltration* (Web application attack)
    - ⚠️ *Mirai / C2 Botnet Beacon* (Periodic command & control heartbeat)
  - **Live Shannon Entropy Meter**: Real-time calculation of $H(X) = -\sum P(x) \log_2 P(x)$ on payload strings.
- **Mode B: Upload Network Data (File / Batch Processor)**:
  - Drag-and-drop support for `.csv`, `.json`, `.txt`, and `.pcap` logs.
  - Bundled 8-record sample KDD-CUP99 / CIC-IDS2017 dataset.
  - Client-side parser with batch inference classification.

### 4. `AI/ML Analysis` (Multi-Stage Ensemble Pipeline)
- **Stage 01: Feature Extraction & Scaling**: Normalizes 14 network flow dimensions with `StandardScaler` tensor mapping.
- **Stage 02: Ensemble Model Inference**:
  - **Random Forest Classifier (100 Trees)**: Evaluates decision paths and probabilistic multi-class attack classification.
  - **Deep Autoencoder Anomaly Detector**: Computes reconstruction loss $L_2$ against the baseline network manifold (0.35 threshold).
- **Stage 03: Explainable AI (XAI / SHAP)**: Visual feature attribution bars indicating whether each metric pushed the score toward Intrusion (red) or Normal (green).
- **Diagnostic Terminal Console**: Millisecond timestamped inference telemetry log.

### 5. Decision Matrix: `Normal Traffic` OR `Intrusion Detected`
- **Case A: Normal Traffic**:
  - Glowing Emerald Shield (`#00e676`).
  - High confidence index (99.4%), low anomaly coefficient (0.038 / 1.00), verified RFC compliance.
- **Case B: Intrusion Detected**:
  - Pulsating Crimson Warning Halo (`#ff1744`) with alarm siren.
  - Threat classification, severity rating (`CRITICAL` / `HIGH`), MITRE ATT&CK reference (e.g. `T1498.001`), and attacker IP.

### 6. `Alert + Report` (SOAR Containment & Forensic Document)
- **Active Alert Hub**: High-priority alert banner with audio klaxon and acknowledgment button.
- **Automated SOAR Playbook**:
  - *Firewall IP Drop*: Generates inline `iptables`, `nftables`, and AWS WAF CLI rules.
  - *Isolate Host/Subnet*: Quarantine VLAN switch port.
  - *Token Bucket Rate Limiting*: Restricts source to 1 pkt/sec.
  - *Canary Honeypot Divert*: Captures zero-day payloads.
- **Printable Audit-Grade Incident Report**: Formatted paper report with Executive Summary, Flow Diagnostics table, XAI decision log, and remediation steps.
- **Export Options**: Print / Save PDF and Export SIEM JSON.

---

## Running Locally

The application runs with zero external npm dependencies via Node.js:

```powershell
# Navigate to the project directory
cd C:\Users\Student\.gemini\antigravity-ide\scratch\ai-ids-sentinel

# Start the local server
node server.js
```

Open your browser to:
**`http://localhost:3000`**
