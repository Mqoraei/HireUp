# HireUp – AI-Powered Initial Candidate Screening

**HireUp** is an AI-driven **pre‑interview screening system** designed to automate and enhance the **initial candidate assessment** process — before human interviews begin.  

This repository contains the **sanitized workflow export** of HireUp, implemented as a **state-machine orchestrated system** using **n8n**, powered by **LLMs**, and delivered through a **Telegram bot** for fast, low-friction validation.


## 🚩 What Problem HireUp Solves

HR teams spend a disproportionate amount of time on early-stage screening:

- Reviewing large volumes of irrelevant or inflated résumés  
- Handling unstructured CV formats  
- Running repetitive, low-signal initial calls  

These pain points lead to **slow hiring**, **inefficient shortlisting**, and **HR fatigue**.  
HireUp focuses **exclusively** on removing this bottleneck.

---

## ⚙️ What HireUp Does

HireUp runs a **short, structured, time-bounded screening** between résumé collection and in-person interviews.

For each candidate, the system:

1. Collects the **target job role**  
2. Asks one **HR (behavioral/situational)** question  
3. Evaluates the HR response using an **LLM**  
4. Asks one **role-specific technical** question  
5. Evaluates the technical response  
6. Produces **explainable scores (1–10)** and a **decision-ready summary** for HR  

> 💬 *This is screening, not interviewing.*

---

## 🧩 Core Design Principles

- **State-machine driven:** deterministic flow, no skipped steps  
- **Time-controlled:** strict response windows with automatic timeouts  
- **Role-aware prompting:** questions adapt to the position applied for  
- **Explainable evaluation:** written analysis + numeric scoring  
- **Human-in-the-loop:** AI assists decisions, not replaces HR judgment  

---

## 🏗️ System Overview

| Component | Role |
|------------|------|
| **Telegram** | Candidate interface |
| **n8n** | Workflow orchestration & state management |
| **LLM (OpenAI-compatible)** | Question generation & evaluation |
| **Supabase** | Persistent session state & data storage |
| **Email (OAuth)** | Delivery of screening reports to HR |

---

## 🔐 Security & Credentials

This repository contains a **sanitized workflow export** intended for public sharing.  
All sensitive credentials (API keys, OAuth tokens, service secrets) have been **removed** and replaced with **clear placeholders** in the JSON file.

**Example placeholders:**

SUPABASE_CREDENTIAL_PLACEHOLDER

GOOGLE_OAUTH_PLACEHOLDER

LLM_API_KEY

TELEGRAM_BOT_TOKEN

These placeholders indicate where real credentials must be configured locally in n8n before execution.

No real API keys, tokens, or personal accounts are included in this repository.

Why This Project Matters

HireUp demonstrates:

Applied LLM system design (not prompt-only usage)

Explicit state and session management

Production-aware handling of time, memory, and security

Focus on real, validated HR pain points

