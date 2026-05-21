# SenIntell Aegis

<p align="center">
  <img src="./Gemini_Generated_Image_7d9q5w7d9q5w7d9q.jpg" alt="SenIntell Aegis Logo" width="550"/>
</p>

<p align="center">
  <strong>An autonomous, localized SOAR platform engineered to intercept high-frequency attack vectors, orchestrate sub-second stateful firewall containment, and leverage a memory-resident, air-gapped LLM layer for instant forensic log auditing.</strong>
</p>

---

## System Architecture Overview

Unlike passive intrusion detection systems or cloud-dependent security tools, **SenIntell Aegis** operates natively at the system infrastructure layer. It bridges low-level Linux kernel networking, persistent background daemons, asynchronous network orchestration, and localized machine learning inference into a deterministic, high-velocity active defense loop.

[ Unblinked Log Ingestion ]  --> Stream live syslog packets (/var/log/auth.log)
│
▼
[ Automated Interception ]    --> Identify high-frequency multi-threaded anomalies (e.g., Hydra)
│
▼
[ Stateful Containment ]     --> Sub-second firewall manipulation (UFW) to isolate adversary
│
▼
[ Threat Intel Enrichment ]  --> Query external OSINT telemetry arrays via AbuseIPDB API
│
▼
[ Air-Gapped AI Audit ]       --> Dispatch contextual metadata arrays to local Llama3 engine
│
▼
[ Immutable Reporting ]       --> Compile structural Markdown forensic audit sheets instantly
│
▼
[ Self-Healing Cool-down ]    --> Asynchronous threading timer automatically triggers IP release


---

## Core Engineering Features

* ⚡ **Sub-Second Perimeter Hardening:** Intercepts threat payloads and programmatically updates the Linux kernel packet-filtering tables using `ufw` to drop malicious source IPs mid-stream.
* 🌐 **Threat Intelligence Enrichment:** Leverages the **AbuseIPDB API** to fetch real-time global telemetry, including the attacker's country of origin, ISP network owner, and global abuse confidence score before auditing.
* 🛡️ **Air-Gapped Forensic Intelligence:** Eliminates data exfiltration risks and external network latency by running an entirely local, sandboxed `llama3` instance via Ollama to generate forensic audits.
* ⏳ **Self-Healing Cooldown Loop:** Utilizes Python asynchronous threading routines to run a non-blocking countdown timer, automatically resetting the perimeter and lifting the firewall block gracefully after a set cool-down window.
* ⚙️ **Process Persistence:** Managed via native background system daemons, guaranteeing 24/7 infrastructure monitoring and automatic crash recovery loops.

---

## The Technical Stack

* **Core Engine:** Python 3.12+ (Threading, Event Streaming, Subprocess Ingestion, Async Timers)
* **Perimeter Defense:** Netfilter / Uncomplicated Firewall (`UFW`)
* **External Threat Intel:** AbuseIPDB v2 JSON API REST Integration
* **Localized Inference Engine:** Ollama Framework (`llama3:latest` parameter execution)
* **Log Ingest Matrix:** Linux System Architecture Logs (`/var/log/auth.log`)

---

## Repository Blueprint

```text
├── config/                  # Operational thresholds and API configuration profiles
├── incident_reports/        # Output directory for generated Markdown audits
├── logs/                    # Internal engine operation logs
├── .gitignore               # System environment exclusion array
├── README.md                # System documentation matrix
├── requirements.txt         # Package dependency array
├── soc_soar_engine.py       # Core background service daemon
└── instant_test.py          # High-speed pipeline execution script
⚡ Quick Deployment Pattern
1. Provision Your Environment
Ensure your local system dependencies are fully initialized:

Bash
sudo apt update && sudo apt install ufw ollama -y
ollama run llama3
2. Configure Your Threat Intel Key
Create a config directory and set up your AbuseIPDB API configuration profile:

Bash
mkdir config
echo "ABUSEIPDB_API_KEY=YOUR_ACTUAL_API_KEY_HERE" > config/credentials.env
3. Initialize and Launch the Platform
Clone the platform array and prepare the isolated environment:

Bash
git clone [https://github.com/Sxfxl05/SenIntell-Aegis.git](https://github.com/Sxfxl05/SenIntell-Aegis.git)
cd SenIntell-Aegis
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
4. Trigger Active Defense Pipeline
Execute the pipeline simulation runner with administrator privileges to link with the kernel firewall rules:

Bash
sudo venv/bin/python instant_test.py
📊 Sample Executive Audit File Output
When an attack vector is successfully neutralized, SenIntell Aegis instantly drops a formatted incident report into incident_reports/:

🛑 INCIDENT AUDIT REPORT: [ID-98431]
Mitigation Status: SUCCESSFUL (Host Isolated)

Adversary Vector Source: 185.122.105.11

Intercept Target Boundary: SSH / Port 22

Target Kernel Directive: ufw deny from 185.122.105.11 to any

Asynchronous Cooldown State: Running (30-Minute Network Restitution Timer Initialized)

🌐 Global Threat Intelligence Matrix
Origin Country: Unknown / Proxy Node

Network Owner (ISP): DigitalOcean LLC

Global Abuse Confidence Score: 98% (High-Risk Threat Actor Match)

AI Forensic Analysis Matrix:
The telemetry array indicates an aggressive, multi-threaded dictionary-based brute-force exploit matching signature parameters of automated scanning tooling (e.g., Hydra). The host layer reacted deterministically within 420ms to eliminate lateral movement risk. External reputation matrices confirm this endpoint is an active, compromised public cloud VPS.

📜 License & Disclaimers
Distributed under the MIT License. Developed independently for enterprise endpoint resilience architecture.
