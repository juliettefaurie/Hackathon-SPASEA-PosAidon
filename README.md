# PosAidon 🛰️

**1st place — SPASEA 2025** · 24h hackathon organized by ENSTA Bretagne, Naval Group & DGA (Brest, December 2024)

The challenge: build an AI agent to help naval operators exploit AIS, RF, and satellite data tactically.

---

## What it does

PosAidon is an interactive dashboard that lets operators track, analyze, and report on vessel behavior in the Mediterranean.

**Vessel tracking**
- Live map with 35+ layers (bathymetry, EEZ zones, vessel density, sea temperature, satellite imagery...)
- Overlay RF detections from Unseenlabs satellites and CNES satellite trajectories
- Select one or several vessels and replay their full trajectory with an animated timeline

**Suspicion detection**
- Flags vessels with abnormal speed (too fast, drifting, or stopped unexpectedly)
- Detects vessels emitting an RF signal with no corresponding AIS — a classic dark vessel pattern
- Cross-references AIS positions with RF detections to identify potential spoofing or evasion
- Scores vessels based on behavioral anomalies and highlights them on the map

**Operator report (PDF)**
- Generates a PDF report for the on-duty officer summarizing a vessel of interest
- Includes: recent trajectory, speed history, suspicious behavior flags, current position, and vessel metadata
- Designed to be actionable — one click, ready to hand off

**AI assistant**
- Ask questions in natural language about any vessel in the dataset
- The agent (LangChain/LangGraph + Grok) queries live data before answering
- Examples: *"Is vessel MMSI 227XXXXXX behaving normally?"*, *"Which vessels have no AIS in this zone?"*

---

## Stack

- **Python** — pandas, folium, ipywidgets
- **AI agent** — LangChain, LangGraph, OpenRouter (Grok)
- **Data** — AIS + RF + ephemerides via DAWEX Space Data Marketplace
- **Map layers** — EMODnet, NOAA, GEBCO, Marine Regions
- **Environment** — Google Colab

---

## Getting started

```bash
pip install langchain langchain-openai langgraph folium ipywidgets geopy pandas pyarrow
```

Set your API keys in the config cell (OpenRouter, OpenWeather, DAWEX credentials), then run the notebook top to bottom.

> The `.parquet` data files are not included — they were provided under the hackathon's data agreement.

---

## Contributors

| | | | | |
|---|---|---|---|---|
| [@Metimer](https://github.com/Metimer) | [@Chakibprojects](https://github.com/Chakibprojects) | @contributor3 | @contributor4 | @contributor5 |
