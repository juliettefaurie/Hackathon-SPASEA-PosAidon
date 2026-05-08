# 🔱 PosAIdon - Assistant Naval Augmenté (LLM & Data Fusion)
**🏆 Vainqueur du 1er Prix - Hackathon SPASEA (Naval Group / DGA)**

![Badge Victoire](https://img.shields.io/badge/Award-1st%20Prize-gold?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![IA](https://img.shields.io/badge/AI-LLM%20%26%20RAG-red?style=for-the-badge)

## 🌊 Le Challenge
Comment aider les marins à repérer des **"Dark Vessels"** (navires suspects avec coupure AIS ou trajectoires anormales) dans l'immensité de l'océan ? 

Face à 10 équipes issues de l'IMT Atlantique, de l'École Navale et de l'ENSTA Bretagne, notre équipe **PosAIdon** a développé une solution d'aide à la décision opérationnelle récompensée pour sa pertinence et sa faisabilité technique.

## 💡 La Solution : L'Intelligence au service de l'Action
Plutôt que d'ajouter une couche de données supplémentaire, nous avons créé un outil qui **fusionne** et **analyse** l'information pour l'opérateur :

1. **Moteur de Fusion Multi-sources** : Croisement en temps réel des signaux AIS (positions), des signatures Radiofréquences (RF) et des éphémérides satellitaires pour détecter ce qui est invisible à l'œil nu.
2. **Assistant Tactique Intelligent** : Interface de type LLM permettant d'interroger la situation tactique en langage naturel (ex: *"Y a-t-il des comportements anormaux dans la zone B ?"*) et d'obtenir des analyses claires et structurées.

## 🛠️ Stack Technique
* **Langages** : Python (Pandas, Requests)
* **IA / LLM** : Architecture RAG avec intégration de modèles via **OpenRouter (Grok)**
* **Cartographie** : **Folium** (plus de 35 couches de données maritimes : bathymétrie, météo, câbles sous-marins, ZEE)
* **Data** : Ingestion via l'API **Dawex** (Space Data Marketplace)
* **Partenaires Data** : Unseenlabs (RF), Prométhée (Sat), CNES

## 📸 Aperçu du Projet
<p align="center">
  <img src="Assets/Screenshot 2025-12-05 11.11.55.png" width="45%" alt="Vue Cartographique Tactique">
  <img src="Assets/Screenshot 2025-12-05 12.54.08.png" width="45%" alt="Interface Assistant IA">
</p>
<p align="center"><i>Vue de la cartographie tactique et de l'interface conversationnelle.</i></p>

## 📂 Structure du Repository
* `/Notebook/` : Le cœur de l'analyse (Python Notebook) avec la fusion de données et l'agent IA.
* `/Assets/` : Captures d'écran et démonstrations visuelles du projet.

## 🚀 Installation & Sécurité
Ce projet utilise des variables d'environnement pour la gestion des clés API.

1. **Clonez le repo** :
   ```bash
   git clone [https://github.com/TonPseudo/Hackathon-SPASEA-PosAIdon.git](https://github.com/TonPseudo/Hackathon-SPASEA-PosAIdon.git)
