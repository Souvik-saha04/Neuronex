
# 🏥 NEURONEX
### *Smart India Hackathon 2025 — Team Neuronex*

> A unified AI-powered digital health platform for India's migrant worker population — ensuring seamless, secure, and multilingual access to healthcare records, disease tracking, and government health interventions across state boundaries.

![SIH 2025](https://img.shields.io/badge/Smart_India_Hackathon-2025-orange?style=for-the-badge&logo=india)
![Health Tech](https://img.shields.io/badge/Health_Tech-AI_Powered-red?style=for-the-badge&logo=heart)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)
![Languages](https://img.shields.io/badge/Languages-5_Supported-blue?style=for-the-badge)
> 🔍 Curious to explore NEURONEX in detail?  
> 👉 **[Click here to view the complete project](https://souvik-saha04.github.io/Neuronex/)**
---

## 📌 Table of Contents

- [About](#-about)
- [Three Interfaces](#-three-interfaces)
- [Live Prototypes](#-live-prototypes)
- [Role-Based Access](#-role-based-access-system)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [System Architecture](#-system-architecture)
- [Feasibility & Viability](#-feasibility--viability)
- [Impact & Benefits](#-impact--benefits)
- [Team](#-team)

---

## 🔍 About

Millions of migrant workers in India lose **continuity of care** every year when they move between states. Neuronex solves this through:

- 🪪 A **portable digital health ID** (Aadhaar-linked)
- 🤖 **AI-driven outbreak detection** and predictive health alerts
- 📄 **OCR-powered prescription intake** for printed documents
- 🏛️ A **three-tier role-based access system** connecting workers, hospitals, and government

**Supported Languages:** Malayalam · Hindi · Bengali · Tamil · English

---

## 📱 Three Interfaces

Neuronex ships three distinct interfaces for three distinct audiences:

| Interface | Audience | Description |
|-----------|----------|-------------|
| 📱 **Mobile App UI** | Migrant Workers | Lightweight, multilingual, offline-capable. Workers carry their digital health ID across states. |
| 🌐 **Web UI** | Workers without smartphones | Full-featured browser-based portal with the same capabilities as the mobile app. |
| 🛡️ **Admin UI** | Hospital Admins & Super Admins | Powerful dashboard with full data access, OCR prescription uploads, user management, and reporting. |

---

## 🚀 Live Prototypes

| Interface | Link | Status |
|-----------|------|--------|
| 🛡️ Admin Side (Hospital / Super Admin) | [**→ Open Admin UI**](https://github.com/Souvik-saha04/neuronex-admin.git) | 🟢 Live |
| 📱 Client Side (User / Mobile pages) | [**→ Open Client UI**](https://github.com/Souvik-saha04/neuronex-user.git) | 🟢 Live |

> ⚡ Click the links above to explore the working prototypes.

---

## 🔐 Role-Based Access System

The platform uses a **three-tier role hierarchy** with encrypted data and granular permission controls:

| Role | Scope | Key Permissions |
|------|-------|-----------------|
| 🔴 **Super Admin** | Government / Platform-wide | View all data across states · Manage all admins · Monitor activities · Generate outbreak reports · Edit user data (with permission) · Receive AI predictive alerts |
| 🔵 **Admin** | Hospital / District | View all user data in jurisdiction · Upload & scan prescriptions via OCR · Verify documents · Edit records (with permission) · Manage Worker Registry |
| 🟢 **User** | Individual Worker | Manage own health records · View prescriptions & lab results · Link family group accounts · Receive health alerts · Offline access via Aadhaar digital ID |

> 🔒 All data is **encrypted at rest and in transit** across all access levels.

---

## ✨ Key Features

### For Workers
- 🪪 **Portable Digital Health ID** — Aadhaar-linked, valid across all Indian states
- 📶 **Offline Support** — Works without internet, auto-syncs when connected
- 🌐 **Multilingual Interface** — Malayalam, Hindi, Bengali, Tamil, English
- 👨‍👩‍👧 **Group / Family Accounts** — Authorized members can securely access shared records
- 👁️ **Full Transparency** — View prescriptions, vaccination history, and lab results anytime

### For Government & Hospitals
- 🚨 **Real-time Outbreak Alerts** — AI detects infectious disease hotspots early
- 📄 **OCR Prescription Intake** — Scan printed prescriptions; handwritten ones entered manually
- 📊 **Disease Tracking Dashboards** — Real-time heatmaps and reporting
- 🔄 **Bidirectional Health Protection** — Notifies worker's home-state health department on return
- 🩸 **Blood Analysis AI** — Glucose/diabetic tracking, cardiac risk detection

### AI & Data Layer
- 🧠 **Vector DB (Pinecone)** — Stores health embeddings, fed to AI agent on server request
- 🔗 **LangChain AI Agent** — Generates predictive alerts with do's & don'ts for users and govt
- 🔮 **Early Disease Detection** — AI-enabled community spread prevention
- 💉 **Smart Vaccination Tracking** — Ensures no coverage gaps (TB, measles, polio)

---

## ⚙️ Tech Stack

| Layer | Technology |
|-------|-----------|
| 🖥️ **Frontend** | React / Next.js + Tailwind CSS |
| 🐍 **Backend** | Django + Django REST Framework |
| 🐘 **Database** | PostgreSQL |
| ⚡ **Caching & Queue** | Redis + Celery |
| 🔥 **Authentication** | Firebase Auth |
| ☁️ **File Storage** | Cloudinary / AWS S3 |
| 🧠 **AI Layer** | LangChain + Pinecone (Vector DB) |
| 🔍 **OCR** | Tesseract / Google Vision API |
| 🗺️ **Maps** | Mapbox / Leaflet |
| 📨 **Notifications** | Firebase Cloud Messaging |
| 🐳 **DevOps** | Docker + Nginx |

---

## 🔄 System Architecture

### Worker Registration & Records
```
Worker Registration → Worker Management → Worker & Registry Data Store → Alerts & Reporting → Weekly Reports
```

### Medical Records Pipeline
```
Selected Worker ID → Health & Medical Records Store → Alerts & Reporting → Show Alerts
```

### Document Management
```
Document Upload Request → Document Management → Documents Repository Store → Display Document
```

### AI Prediction Pipeline
```
Health Data → Vector DB (Pinecone) → LangChain AI Agent → Predictive Alert → Govt + User Notifications
```

### Prescription Intake
```
Printed Prescription → OCR Scan (Google Vision / Tesseract) → AI Processing → Secure DB Storage
Handwritten Prescription → Manual Admin Entry → Secure DB Storage
```

---

## 📊 Feasibility & Viability

### ✅ Why It Works
- Lightweight frameworks with **offline-first** local storage for low-connectivity areas
- MVP buildable at **low cost** using open-source tools
- **API-based integration** with existing state e-health platforms (e.g. Kerala)
- Scalable with support from government agencies and NGOs

### ⚠️ Challenges & How We Address Them

| Challenge | Our Approach |
|-----------|-------------|
| States already have partial e-health systems | API bridges for seamless integration |
| Duplicate profiles & incorrect entries | Aadhaar + biometric validation + admin verification |
| Low income — direct monetization is hard | Free for migrants; funded via NGOs, CSR & government programs |
| Data privacy across three access levels | Full encryption + permission-based access control |

### 💰 Sustainability Model
- Free for all migrant workers
- Funded through: **Government programs · NGOs · CSR initiatives · Institutional hospital partnerships**

---

## 🌍 Impact & Benefits

### Impact on Migrant Workers
- Access to personal health records **anytime, anywhere** — no dependency on physical files
- **Continuity of care** when moving between states or jobs
- Transparency into prescriptions, lab results, and vaccination history
- Greater **empowerment** and control over personal health data

### Impact on Public Health System
- **Disease Outbreak Control** — Early detection via real-time dashboards and heatmaps
- **Vaccination Tracking** — Ensures no gaps in coverage for TB, measles, polio
- **Data-driven Policy** — Health authorities make decisions based on reliable migrant data

### Broader Benefits
- 📉 Reduced disease transmission — protects local communities from outbreaks
- 💸 Lower healthcare costs — prevention reduces hospital burden
- 🌐 Multilingual access — workers from all regions can use the app easily
- 🎯 Supports **UN SDGs** — improves health outcomes and reduces inequalities
- ⚖️ Ensures **fair and impartial healthcare access** for all migrant workers

---

## 👥 Team

**Team Neuronex** — Smart India Hackathon 2025

Building at the intersection of **AI, public health, and social impact** — to ensure no migrant worker is left behind in India's healthcare system.

---

<div align="center">

Made with ❤️ by **Team Neuronex** &nbsp;|&nbsp; Smart India Hackathon 2025

![Migrant Health](https://img.shields.io/badge/Migrant_Health-Platform-red?style=flat-square)
![AI Powered](https://img.shields.io/badge/AI-LangChain_+_Pinecone-purple?style=flat-square)
![Django](https://img.shields.io/badge/Backend-Django-green?style=flat-square)
![React](https://img.shields.io/badge/Frontend-React_/_Next.js-blue?style=flat-square)
![PostgreSQL](https://img.shields.io/badge/DB-PostgreSQL-lightblue?style=flat-square)

</div>
