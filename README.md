# PosAIdon - Augmented Naval Assistant (LLM & Data Fusion)
** 1st Prize Winner - SPASEA Hackathon (Naval Group / DGA)**

![Badge Victoire](https://img.shields.io/badge/Award-1st%20Prize-gold?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![IA](https://img.shields.io/badge/AI-LLM%20%26%20RAG-red?style=for-the-badge)

## The Challenge
How can we help naval operators spot **"Dark Vessels"** (suspicious ships with disabled AIS or abnormal trajectories) in the vastness of the ocean?

Competing against 10 teams from IMT Atlantique, École Navale, and ENSTA during this 24h hackathon, our team **PosAIdon** developed an operational decision-support dashboard that was rewarded for its tactical relevance and technical feasibility.

## The Solution: Intelligence in Action
Rather than just adding another data layer, we created an interactive tool that **fuses** and **analyzes** information for the operator:

1. **Multi-source Data Fusion & Tracking**: Real-time cross-referencing of AIS signals, Radio Frequency (RF) signatures, and satellite ephemerides to detect what is invisible to the naked eye. Features a live map with animated trajectory replays.
2. **Suspicion Detection**: Flags vessels with abnormal speeds (drifting, unexpectedly stopped), detects RF signals with no corresponding AIS (classic dark vessel pattern), and scores vessels based on behavioral anomalies to identify potential spoofing.
3. **Intelligent Tactical Assistant**: An AI agent allowing operators to query the tactical situation in natural language (e.g., *"Is vessel MMSI 227XXXXXX behaving normally?"* or *"Which vessels have no AIS in this zone?"*).
4. **Operator Report (PDF)**: One-click PDF report generation summarizing a vessel of interest (history, anomalies, current position) ready to be handed off to the on-duty officer.

## Tech Stack
* **Languages & Core**: Python (pandas, pyarrow, requests, ipywidgets)
* **AI Agent**: LangChain, LangGraph, OpenRouter API (Grok / GPT)
* **Mapping**: **Folium** & Geopy (35+ maritime layers including EMODnet, NOAA, GEBCO, Marine Regions, bathymetry, EEZ, etc.)
* **Data Integration**: Ingestion via **Dawex** API (Space Data Marketplace)
* **Data Partners**: Unseenlabs (RF), Prométhée (Sat), CNES
* **Environment**: Jupyter / Google Colab

## Project Overview
<p align="center">
  <img src="Assets/Screenshot 2025-12-05 11.11.55.png" width="45%" alt="Tactical Map View">
  <img src="Assets/Screenshot 2025-12-05 12.54.08.png" width="45%" alt="AI Assistant Interface">
</p>
<p align="center"><i>Tactical map view and natural language conversational interface.</i></p>

## Repository Structure
* `/Notebook/` : The core analysis (Python Notebook) including data fusion pipelines and the AI agent logic.
* `/Assets/` : Screenshots and visual demonstrations of the project.
* `requirements.txt` : Required dependencies to run the project.

## Getting Started & Security
This project uses environment variables to securely manage API keys.

1. **Clone the repo**:
   ```bash
   git clone [https://github.com/sei22/Hackathon-SPASEA-PosAIdon.git](https://github.com/sei22/Hackathon-SPASEA-PosAIdon.git)
   ```
2. **Install dependencies**
3. **Set up your environment**:
  Create a `.env` file at the root of the project with your API credentials:
  ```bash
  DAWEX_CLIENT_ID=your_id
  DAWEX_CLIENT_SECRET=your_secret
  OPENROUTER_API_KEY=your_key
  ```
---

## Contributors
[Sei BAYLE](https://github.com/sei22), [Juliette FAURIE](https://github.com/juliettefaurie), Charbel DIB, Axel GRUYEZ
