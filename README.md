# 🧠 NeuroAtck

> **Map functionality. Trace the attack surface.**

NeuroAtck is an AI assisted Chrome extension for **web application reconnaissance and security test planning**.

It analyzes the current web page, creates a structured snapshot of the observed application, sends the data to a selected AI provider, and maps the application into:

**Functionality → Endpoints → Attack Surfaces → Security Tests**

Designed for authorized penetration testing, security research, CTFs, and security education.

---

## 🏗️ Architecture

```text
                         ┌──────────────────────┐
                         │    Web Application    │
                         │     Current Tab      │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │   Page Snapshot      │
                         │                      │
                         │ Forms                │
                         │ Inputs               │
                         │ Buttons              │
                         │ Links                │
                         │ Scripts              │
                         │ API Hints            │
                         │ Endpoints             │
                         │ Visible Text         │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │     JSON Snapshot    │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │      AI Router       │
                         │      callAI()         │
                         └──────────┬───────────┘
                                    │
               ┌────────────────────┼────────────────────┐
               │                    │                    │
               ▼                    ▼                    ▼
        ┌─────────────┐      ┌─────────────┐      ┌─────────────┐
        │   Ollama    │      │    Groq     │      │ Gemini/OpenAI│
        │  Local AI   │      │  Cloud AI   │      │  Cloud AI   │
        └──────┬──────┘      └──────┬──────┘      └──────┬──────┘
               │                    │                    │
               └────────────────────┼────────────────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │     AI Analysis      │
                         │                      │
                         │ Functionality        │
                         │ Endpoints            │
                         │ Attack Surfaces      │
                         │ Security Tests       │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │     NeuroAtck UI     │
                         │                      │
                         │ Attack Surface       │
                         │ Functions            │
                         │ Endpoints            │
                         │ Tests                │
                         └──────────────────────┘



🚀 Installation

-Download NeuroAtck.zip and unzip it
-Visit chrome and seach chrome://extensions
-Enable Developer Mode
-Load unpacked
-Add api (NeuroAtck → Settings)
-Now scan your app 

                         
