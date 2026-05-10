# AI Photo Mentor — Project Profile

> **BSc Final Year Research Project · SLIIT 2026 · SE4051 — Trends in Digital Media**

A mobile Vision-Language system that delivers professional-grade photography critique in under 15 seconds, powered by a fine-tuned Qwen2-VL-2B model running on cloud infrastructure.

🌐 **Live Site:** [dulshan2000.github.io/-AI-Photo-Mentor-Project-Profile](https://dulshan2000.github.io/-AI-Photo-Mentor-Project-Profile/)

---

## 📌 About

AI Photo Mentor bridges the gap between amateur photographers and expert feedback. Users capture or import a photo through an Android app and receive structured critique across three dimensions — **Composition**, **Lighting**, and **Technical Quality** — each with a score, critique text, and actionable improvement steps.

| Metric | Result |
|--------|--------|
| Structured output rate | 98.4% |
| Expert correlation (Spearman ρ) | 0.72 |
| Cost per critique | < $0.01 |
| Avg. response time | < 15 seconds |

---

## 🔗 Project Resources

| Resource | Link |
|----------|------|
| 📱 Android App Source | [github.com/dulshan2000/AI-Photo-Mentor](https://github.com/dulshan2000/AI-Photo-Mentor) |
| 💾 RPCD-Elite-5K Dataset | [kaggle.com/datasets/dulshanbandara/rpcd-elite-5k-v4](https://www.kaggle.com/datasets/dulshanbandara/rpcd-elite-5k-v4) |
| ⚙️ Fine-Tuned GGUF Model | [huggingface.co/dulshanbandara/qwen2vl-2b-photography-critique-GGUF](https://huggingface.co/dulshanbandara/qwen2vl-2b-photography-critique-GGUF) |
| 🏋️ Fine-Tuning Notebook | [kaggle.com/code/dulshanbandara/qwen2-vl-2b-fine-tuning-for-ai-photography-critiqu](https://www.kaggle.com/code/dulshanbandara/qwen2-vl-2b-fine-tuning-for-ai-photography-critiqu) |
| ⚡ Inference Server Notebook | [kaggle.com/code/dulshanbandara/qwen2vl-inference](https://www.kaggle.com/code/dulshanbandara/qwen2vl-inference) |
| 📑 Conference Paper | [AI_Photo_Mentor_Conference_Paper.pdf](./AI_Photo_Mentor_Conference_Paper.pdf) |

---

## 🏗️ System Architecture

```
Android App (Kotlin + Compose)
        │
        │  multipart/form-data POST /critique
        ▼
FastAPI Server (Cloud / Kaggle)
        │
        │  llama-cpp-python
        ▼
Qwen2-VL-2B GGUF (Q4_K_M)
Fine-tuned on RPCD-Elite-5K
```

**Mobile Stack:** Kotlin · Jetpack Compose · CameraX · Retrofit · Room · Hilt  
**Backend Stack:** FastAPI · llama-cpp-python · ngrok  
**Model:** Qwen2-VL-2B-Instruct · LoRA fine-tuning · GGUF quantization (Q4_K_M)

---

## 📊 Dataset — RPCD-Elite-5K

- **Source:** 31,983 posts from r/photocritique (Reddit)
- **Final size:** ~5,000 image–critique pairs (3,504 used for training)
- **Annotations:** Composition · Lighting · Technical scores + critiques + improvement steps
- **Synthesis:** Gemma 4 31B (Google)
- **License:** CC BY-SA 4.0

---

## 👤 Researcher

**Bandara W.K.D.H.K** · IT22572660  
BSc (Hons) Information Technology — Specializing in Interactive Media  
Sri Lanka Institute of Information Technology · 2026  
**Supervisor:** Mr. Ishara Gamage
