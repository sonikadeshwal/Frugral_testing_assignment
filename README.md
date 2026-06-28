# 🧪 Frugal Testing — AI-Native Software Engineer Intern Assignment

> **Candidate:** Sonika Deshwal  
> **University:** Lovely Professional University  
> **Registration No:** 12312987  
> **Role:** AI-Native Software Engineer Intern  
> **Company:** Frugal Testing & BuildNexTech  

---

## 📌 Overview

This repository contains my complete submission for the **Frugal Testing AI-Native Software Engineer Intern** technical assignment. The assignment evaluates AI-assisted engineering, automation testing, and systems thinking across two sections:

- **Section A** — Practical automation engineering (Python + Playwright + Node.js)
- **Section B** — Scenario-based AI reasoning, systems analysis, and architectural thinking

---

## 📁 Repository Structure

```
frugal-testing-assignment/
│
├── q1/
│   ├── canvas_server.js        # WebSocket + HTTP testbed server
│   ├── canvas_page.html        # HTML5 Canvas streaming page
│   └── test_q1_canvas.py       # Playwright automation script
│
├── q2/
│   ├── mock_api_server.js      # Express API with HMAC-SHA512 + replay protection
│   └── test_q2_replay.py       # Cryptographic replay testing script
│
├── q3/
│   └── q3_shadow_dom_and_cot.py  # Shadow DOM traversal + CoT prompt
│
└── README.md
```

---

## ⚙️ Section A — Automation Tasks

### Q1 — Dynamic HTML5 Canvas State Drifts & Asynchronous Race Interceptions

**Tech Stack:** Python, Playwright, Node.js, WebSockets

**What it does:**
- Builds a local HTML5 Canvas WebSocket testbed streaming live color state updates
- Intercepts WebSocket packets and injects **Fibonacci-sequence jitter delays** (1000ms × step, capped at 8000ms)
- Uses a custom **pixel-color polling engine** via `requestAnimationFrame` to detect canvas state transitions without static delays
- Fires a **race injection sequence** (Hover → Drag 15px → Click) within a 30–100ms window with a circuit-breaker macro
- Injects corrupted boundary payloads (`1e+7`, `NaN`, `Infinity`) and asserts frontend exception boundary behavior

**How to run:**
```bash
# Terminal 1 — Start WebSocket testbed server
cd q1
npm install ws express
node canvas_server.js

# Terminal 2 — Run Playwright automation
pip install playwright
playwright install chromium
python test_q1_canvas.py
```

---

### Q2 — Cryptographic Replay Testing, Stateful Nonces & Hash-Chain API Chaining

**Tech Stack:** Python, Requests, Node.js, Express, HMAC-SHA512

**What it does:**
- Builds a local Express API server that issues cryptographic challenge nonces on transaction creation
- Dynamically generates **HMAC-SHA512** authentication headers using a microsecond timestamp + salt sequence
- Fires a **replay attack** within 150ms using the identical payload and MAC token
- Asserts that the backend correctly returns **HTTP 409 Conflict** for duplicate nonce detection
- Flags a critical vulnerability alert if the backend mistakenly accepts the replay

**How to run:**
```bash
# Terminal 1 — Start mock API server
cd q2
npm install express
node mock_api_server.js

# Terminal 2 — Run replay test
pip install requests
python test_q2_replay.py
```

**Expected output:**
```
[SPEC 1] Transaction created → 201 ✓
[SPEC 2] HMAC verified → 200 ✓
[SPEC 3] Replay fired in ~5ms
[SPEC 4] Replay rejected → 409 ✓ ASSERTION PASS
```

---

### Q3 — Sealed Closed-Boundary Shadow DOM Pathfinding & Accessibility Tree Refactoring

**Tech Stack:** Python, JavaScript

**What it does:**
- Implements a **recursive JavaScript Shadow DOM traversal engine** that pierces both open and closed shadow roots without relying on regenerating class strings
- Locates target elements using stable semantic attributes (`data-qa-state`, `role`, `aria-*`) only
- Constructs a dense **Chain-of-Thought (CoT) system prompt** that trains an LLM to navigate OS Accessibility Tree properties exclusively — forbidding element IDs, XPaths, CSS selectors, and text content matching

**How to run:**
```bash
cd q3
python q3_shadow_dom_and_cot.py
```

---

## 🧠 Section B — Key Topics Covered

| Question | Topic |
|----------|-------|
| Q4 | Multi-Agent Synthesis Pipeline Cascading Drift |
| Q5 | GC Leaks & Microtask Loop Starvation (V8 crash analysis) |
| Q6 | SQL Injection in AI-generated code + Prompt Engineering fix |
| Q7 | Flaky Test Clock-Drift in Ephemeral Cloud Runners |
| Q8 | HikariCP Connection Pool Leak under Distributed Strain |
| Q9 | CSS-in-JS Layout Tree Collapse — False Green Automation |
| Q10 | Agentic Hallucination Loop Detection & Sandboxing |
| Q11 | AST-Driven Intelligent Test Selection Frameworks |
| Q12 | Self-Healing Engine Levenshtein + Graph DOM Analysis |
| Q13 | MCP Zero-Trust Schema Sandboxing |
| Q14 | Asynchronous Log Ingestion at Scale (Kafka + Workers) |
| Q15 | OpenTelemetry Distributed Tracing & Lock Contention |
| Q16 | LLM Context Contraction in Multi-Turn Prompting |
| Q17 | HIPAA Healthcare Platform Quality Engineering Blueprint |
| Q18 | OpenAPI Boundary Exploitation & Semantic Attack Vectors |
| Q19 | AI-Native Automated Release Sign-Off Gates |
| Q20 | Closed-Loop Production-Driven Adaptive Stress Testing |

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python)
![Playwright](https://img.shields.io/badge/Playwright-Automation-green?logo=playwright)
![Node.js](https://img.shields.io/badge/Node.js-Express-brightgreen?logo=node.js)
![WebSocket](https://img.shields.io/badge/WebSocket-ws-orange)
![HMAC](https://img.shields.io/badge/Security-HMAC--SHA512-red)

---

## 🚀 Prerequisites

```bash
# Python packages
pip install playwright requests
playwright install chromium

# Node.js packages (inside q1 and q2 folders)
npm install ws express
```

---

## 👩‍💻 About Me

Hi, I'm **Sonika Deshwal**, a final-year B.Tech CSE student at Lovely Professional University passionate about AI-native engineering, automation testing, and building systems that reason about correctness — not just generate code.

- 🔗 [LinkedIn](https://www.linkedin.com/in/sonikadeshwal/)
- 💻 [GitHub](https://github.com/sonikadeshwal)
- 🏆 [LeetCode](https://leetcode.com/u/Sonika_Deshwal/)
- 🌐 [Live Project](https://fast-upload--sonikajaatdeshw.replit.app/)

---

## 📄 License

This project was created as part of a technical assignment for Frugal Testing & BuildNexTech.  
© 2026 Sonika Deshwal | Lovely Professional University
