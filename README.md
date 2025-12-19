###HireUp – AI-Powered Initial Candidate Screening

HireUp is an AI-driven pre-interview screening system designed to automate and improve the initial assessment of candidates before human interviews begin.

This repository contains the sanitized workflow export of HireUp, implemented as a state-machine-based system orchestrated with n8n, powered by LLMs, and delivered through a Telegram bot interface for fast, low-friction validation.

What Problem HireUp Solves

HR teams spend a disproportionate amount of time on early-stage screening:

Reviewing large volumes of irrelevant or inflated resumes

Handling unstructured CVs

Running repetitive, low-signal initial calls

This results in slow hiring, poor shortlists, and HR fatigue.

HireUp focuses exclusively on this bottleneck.

What HireUp Does

HireUp runs a short, structured, time-bounded screening after resume collection and before in person interviews.

For each candidate, it:

Collects the target job role

Asks one HR (behavioral/situational) question

Evaluates the HR response using an LLM

Asks one role-specific technical question

Evaluates the technical response

Produces explainable scores (1–10) and a decision-ready summary for HR

This is screening, not interviewing.

Core Design Principles

State-machine driven: deterministic flow, no skipped steps

Time-controlled: strict response windows, automatic timeouts

Role-aware prompting: questions adapt to the applied position

Explainable evaluation: written analysis + numeric scores

Human-in-the-loop: AI assists decisions, does not replace HR

System Overview

Telegram – Candidate interface

n8n – Orchestration & state machine

LLM (OpenAI-compatible) – Question generation & evaluation

Supabase – Persistent session state and storage

Email (OAuth) – Delivery of screening reports to HR



Security & Credentials

This repository contains a sanitized workflow export intended for public sharing.

All sensitive credentials (API keys, OAuth tokens, service secrets) have been manually removed from the workflow and replaced with clear placeholders inside the JSON file.

Examples of placeholders used:

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

