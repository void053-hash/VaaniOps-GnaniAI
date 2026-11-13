# VaaniOps: Zero-Touch Industrial Shop-Floor Voice Copilot

**Built by:** Devansh Pandey (M.Sc. Data Science & AI, Nalanda University)  
**Powered by:** Gnani.ai Prisma v3.0 (STT) & Timbre v2.5 (TTS)

## 1. The Problem
Across India's manufacturing, paper recycling, and logistics sectors, thousands of shop-floor technicians communicate machinery breakdowns and shift updates via unstructured Hindi/Hinglish voice notes. Because their hands are occupied or soiled on the floor—and many are uncomfortable typing in English—they cannot enter data directly into ERP dashboards. Critical downtime events get buried in chat threads, causing missed log entries, delayed maintenance, and untracked production losses.

## 2. The Solution
**VaaniOps** is a two-way, hands-free voice copilot that bridges raw shop-floor speech and structured enterprise ERP ledgers using Gnani.ai's Indic speech stack:
* **Listen (`Gnani Prisma v3.0`):** Captures noisy, code-mixed Hindi/English worker voice reports and transcribes them with high accuracy.
* **Structure (`Python Entity Parser & ERP Ledger`):** Extracts the affected department, issue category, downtime hours, and severity level (`CRITICAL` vs. `HIGH`) from the transcript, logging a structured row into a live tabular ledger and updating shift KPIs in real time.
* **Respond (`Gnani Timbre v2.5`):** Synthesizes an immediate, localized Hindi voice confirmation (`Nalini` voice) over the floor speaker, confirming that the log is recorded and maintenance has been alerted.

## 3. Architecture Flow
## 3. Architecture Flow
`Worker Voice Input (WAV/MP3/Mic)` → `Gnani Prisma v3.0 STT` → `Deterministic Entity Extraction` → `Live ERP DataFrame / SQL Ledger` → `Gnani Timbre v2.5 Hindi TTS Confirmation`
## 4. How to Run Locally
```bash
pip install -r requirements.txt
streamlit run app.py 
```