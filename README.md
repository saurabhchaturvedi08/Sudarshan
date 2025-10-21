# 🛡️ Sudarshan — AI-Powered Truth & Trust Network

> **"Cut Through Illusion. See Clearly."**  
> An AI-driven platform to detect misinformation, verify authenticity, and ensure ethical AI usage — powered by multimodal analysis and blockchain-backed trust scoring.

---

## 🚨 Problem

The world is flooded with **AI-generated misinformation, deepfakes, and manipulated content**.  
Businesses, media, and individuals struggle to **distinguish truth from synthetic reality** — eroding trust, causing social harm, and creating legal risk.

---

## 💡 Solution

**Sudarshan** is an AI-powered platform that verifies the authenticity of digital content (text, image, audio, or video) through:

- **AI-powered multimodal verification**
- **Fact-checking through intelligent agents**
- **Blockchain-backed trust scoring for transparency**

> Think of it as the _“Chakra of Truth”_ for the AI era — cutting through fake, manipulated, or unethical content.

---

## 🧩 MVP Features (2–3 Week Build)

| Feature                              | Description                                                                        | Status             |
| ------------------------------------ | ---------------------------------------------------------------------------------- | ------------------ |
| 🧠 **Source Analyzer Agent**         | Extracts metadata, traces origins, and checks credibility of sources.              | ✅ MVP Focus       |
| 🔍 **Deepfake Detector (GPU-based)** | Uses vision + audio models to detect fake/manipulated content.                     | ✅ MVP Focus       |
| 📑 **Fact Validator Agent**          | Cross-verifies claims using trusted datasets/APIs (e.g. Wikipedia, FactCheck.org). | 🔄 In Progress     |
| ⛓️ **Trust Score Engine**            | Generates a blockchain-backed “Trust Index” for every verified file or claim.      | MVP via mock chain |
| 🌐 **API + UI (Cloud Run)**          | Simple web interface + REST API for content upload and verification report.        | ✅ MVP Focus       |

---

## 🏗️ Architecture Overview

```text
                  ┌───────────────────────────────┐
                  │           Frontend (UI)        │
                  │  React / Streamlit (Cloud Run) │
                  └───────────────┬───────────────┘
                                  │
                                  ▼
              ┌───────────────────────────────┐
              │       API Gateway (Cloud Run) │
              │   Handles upload & verification│
              └───────────────┬───────────────┘
                              │
    ┌─────────────────────────┼──────────────────────────┐
    ▼                         ▼                          ▼
┌────────────┐         ┌──────────────┐          ┌────────────────┐
│ Source     │         │ Deepfake     │          │ Fact Validator │
│ Analyzer   │         │ Detector     │          │ (LLM Agent)    │
│ (Agent 1)  │         │ (GPU/Gemma)  │          │ (Agent 2)      │
└────────────┘         └──────────────┘          └────────────────┘
                              │
                              ▼
                    ┌────────────────────┐
                    │ Trust Scorer Agent │
                    │ (Blockchain Layer) │
                    └────────────────────┘
                              │
                              ▼
                   ┌────────────────────────┐
                   │ Verification Report API │
                   └────────────────────────┘
```

---

## ⚙️ Tech Stack

| Layer                       | Technology                                      |
| --------------------------- | ----------------------------------------------- |
| **Frontend**                | Streamlit / React (Cloud Run)                   |
| **Backend / API**           | FastAPI (Python)                                |
| **AI Models**               | Gemma (GPU) / OpenAI / CLIP / Whisper           |
| **Blockchain Layer (Mock)** | Polygon / Ethereum testnet / Local IPFS for MVP |
| **Database**                | Firestore or DynamoDB                           |
| **Deployment**              | Google Cloud Run / AWS Lambda                   |
| **Storage**                 | S3 / GCS for media files                        |

---

## 🚀 MVP Workflow

1. **Upload Content (Text, Image, Audio, or Video)**  
   → File stored in secure bucket.

2. **Source Analyzer Agent**  
   → Extracts metadata, origin, EXIF data, timestamps, and links.

3. **Deepfake Detector (GPU)**  
   → Runs Gemma or other vision model for content authenticity detection.

4. **Fact Validator Agent**  
   → Checks factual consistency against trusted online sources.

5. **Trust Scorer**  
   → Aggregates findings → generates **Trust Index (0–100)**.

6. **Report Generation**  
   → Returns verification summary with confidence score and blockchain reference ID.

---

## 🧠 AI Agent Design

| Agent                    | Role                                            | Model / Tools                       |
| ------------------------ | ----------------------------------------------- | ----------------------------------- |
| 🔍 **Source Analyzer**   | Trace origin, detect metadata anomalies         | Python + metadata parsers           |
| 🧠 **Fact Validator**    | Validate textual/visual claims                  | Gemma / Llama + web search APIs     |
| 🎥 **Deepfake Detector** | Analyze image/video/audio manipulation          | Vision transformer / CLIP / Whisper |
| 🔗 **Trust Scorer**      | Combine agent results + push hash to blockchain | Python + Smart Contract SDK         |

---

## 🧭 Development Roadmap

| Phase                  | Duration    | Focus                                                 |
| ---------------------- | ----------- | ----------------------------------------------------- |
| 🧩 **MVP (Hackathon)** | 2–3 Weeks   | Source Analyzer, Deepfake Detection, Trust Report     |
| ⚡ **Phase 2**         | +1 Month    | Add Fact Validator + Blockchain Trust Record          |
| 🌐 **Phase 3**         | +2–3 Months | Public API, SDK, Chrome Plugin for media verification |

---

## 🎯 Impact

| Audience               | Value                                                     |
| ---------------------- | --------------------------------------------------------- |
| **Individuals**        | Verify if any media or claim is fake or AI-generated.     |
| **Businesses**         | Protect brand reputation & ensure content authenticity.   |
| **Governments / NGOs** | Use trust indices to counter misinformation campaigns.    |
| **Developers**         | Integrate Sudarshan API for automatic media verification. |

---

## 🤝 Hackathon Relevance

| Requirement        | How Sudarshan Fits                        |
| ------------------ | ----------------------------------------- |
| 🧠 **AI Studio**   | Builds verification intelligence pipeline |
| 🤖 **AI Agents**   | Modular fact-checking agents              |
| ⚡ **GPU / Gemma** | Deepfake & multimodal content analysis    |

---

## 🧩 Next Steps

- [ ] Build Source Analyzer Agent (metadata & content type detection)
- [ ] Integrate basic Deepfake detection model
- [ ] Deploy FastAPI backend on Cloud Run
- [ ] Add “Trust Score Report” UI on Streamlit
- [ ] (Optional) Mock blockchain hash storage for MVP

---

## 🧰 Installation (for MVP Demo)

```bash
git clone https://github.com/<your-repo>/sudarshan.git
cd sudarshan

# Setup environment
pip install -r requirements.txt

# Run FastAPI backend
uvicorn app.main:app --reload

# Run Streamlit UI
streamlit run ui/app.py
```

---

## 🪙 License

MIT License © 2025 Sudarshan AI Team

---

## 👥 Contributors

- **Saurabh [Team Lead]** — Architecture, Backend, AI Integration, Frontend, Blockchain, and Research
