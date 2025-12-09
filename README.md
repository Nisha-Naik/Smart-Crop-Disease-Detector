# 🌾 Smart Crop Sentinel – AI-Powered Crop Disease Assistant

> **Smart Crop Sentinel** is a hackathon-built, end-to-end AI web application that allows farmers to **upload a crop leaf image**, automatically **detects the disease**, and provides **complete treatment plans, medicines, application instructions, and “search to buy” links** in both **English and Kannada**.

---

## 📌 Project Overview

Farmers frequently observe unusual spots, discoloration, or decay on crop leaves but struggle to understand:

- What disease the crop is suffering from  
- How severe or fast-spreading it is  
- Which chemical/organic solution to use  
- How to apply the treatment safely  
- Where to purchase the correct fungicide or pesticide  

**Smart Crop Sentinel** solves this gap with a powerful combination of **computer vision (CNN)**, **LLM-driven disease intelligence**, **multilingual translation**, and a **farmer-first UI**.

### ✔ End-to-End Workflow

1. Farmer uploads a **single leaf image** or clicks a live photo.  
2. AI identifies the **crop type** + **disease** with accuracy.  
3. The disease engine generates:
   - Disease name & scientific name  
   - Severity & spread rate  
   - Detailed cause  
   - Step-by-step actionable treatment  
   - Recommended fungicides/pesticides with dosage + safety  
4. “**Search to Buy**” button opens Google with the exact product query (BigHaat, Amazon, Flipkart etc.)  
5. Farmers can **translate** the entire solution into Kannada instantly.  
6. Results are saved automatically in **Analysis History** for future reference.

---

## ✨ Key Features

### 🧠 AI Image-Based Disease Detection
Upload a leaf → AI predicts:
- Crop name  
- Disease name (e.g., *Marssonina Blotch*, *Anthracnose*, *Goss’s Wilt*)  
- Detection accuracy %  
- Disease stage (Mild / Moderate / Severe)  
- Spread rate (Slow / Medium / Rapid)

---

### 📊 Rich Disease Summary Card
Includes:
- Crop & scientific name  
- Accuracy visual bar  
- Severity color indicator  
- Spread rate indicator  

---

### 💊 Recommended Medicines (Fully Explained)
Each recommendation contains:
- Chemical name + branded examples  
- Dosage for:
  - Large-scale agricultural fields  
  - Home garden units  
- Safety precautions  
- Application timing  
- PHI (Pre-Harvest Interval)  
- Reapplication guidelines  
- Collapsible UI to maintain cleanliness

---

### 🛒 Search to Buy Integration
One click → opens Google search:



Farmer sees:
- BigHaat prices  
- Agribegri stock  
- Amazon/Flipkart options  
- Local nearby store results  

---

### 🌍 Multilingual Translation (English + Kannada)
Every content block (solution, cause, steps, medicines) has a **Translate** dropdown with:
- Hindi  
- Bengali  
- Tamil  
- Telugu  
- Marathi  
- Kannada  

Perfect for real-world farmer adoption.

---

### 🚜 Actionable Steps (Farmer-Friendly)
Solutions include:
- Sanitation  
- Pruning & air circulation  
- Irrigation management  
- Preventive control measures  
- Seasonal advice  

Clear, numbered, and extremely easy to follow.

---

### 🔥 Premium “AI Analyzing…” Experience
A futuristic scanning UI:
> “AI Analyzing… Initiating quantum-neural scan…”

This enhances hackathon impact and real-world UX.

---

### 🔁 Analysis History
Stores:
- Disease image  
- Detected crop  
- Disease name  
- Date  
- Severity & accuracy  
Farmers can revisit all past detections.

---

## 🧠 How It Works (End-to-End Flow)

1. **Upload Image**  
   The user uploads/drag-drops the crop leaf image.

2. **AI Vision Model Classifies Disease**  
   A CNN or vision model identifies crop + disease label.

3. **LLM Knowledge Engine Generates Explanation**  
   It creates:  
   - Disease cause  
   - Treatment strategy  
   - Recommended medicines  
   - Actionable steps  

4. **Translation Service**  
   Converts content to Kannada or any supported language.

5. **Search-to-Buy Link Builder**  
   Forms queries like:  
   `buy Mancozeb M-45 fungicide`

6. **Client-side History Storage**  
   Saves analysis items for easy access.

---

## 🏗️ Architecture

### **Frontend (Next.js App Router)**
- Next.js 14  
- React 18  
- Tailwind CSS  
- shadcn/ui  
- Lucide Icons  
- TypeScript  
- (Optional) Framer Motion animations  

### **AI & Backend**
- Vision model → Classifies diseases  
- LLM-based generator → Creates treatment, medicine list, explanations  
- Translation model → Kannada + multilingual support  
- API handler → `/api/analyze` handles:
  - Image conversion  
  - AI calls  
  - Data merging  
  - Error handling  

### **Persistence**
- Client-side history (local storage) for demo environment  
- Can scale to Firebase / PostgreSQL later

---

## 🧪 User Journey (Demo Script)

1. Home → Click **Start Analysis**  
2. Upload leaf image  
3. AI analyzing screen  
4. Full disease report appears  
5. Translate to Kannada  
6. Expand medicine card  
7. Click “Search to Buy”  
8. Visit analysis history  

This script is perfect for hackathon presentations.

---

## 🛠 Tech Stack

### 🟩 Frontend
- Next.js  
- React  
- Tailwind CSS  
- shadcn/ui  
- Lucide Icons  
- TypeScript  

### 🧠 Backend + AI
- AI Image Classification Flow  
- AI Solution Generation Flow  
- AI Translation Flow  
- Next.js API Routes  

### 🗄 Hosting / Deployment
- Firebase Hosting  
- Firebase Studio development environment  
- Environment-managed secrets  

---

## 📂 Project Structure (High-Level)

```
smart-crop-sentinel/
│
├─ public/
│ └─ images/ # Icons, leaf examples, branding
│
├─ src/
│ ├─ app/
│ │ ├─ page.tsx # Hero + Upload + Home sections
│ │ ├─ analysis/ # Analysis result page
│ │ ├─ history/ # History page
│ │ └─ api/
│ │ └─ analyze/ # AI analysis API route
│ │
│ ├─ components/ # Cards, UI widgets, loaders
│ ├─ lib/
│ │ ├─ ai/ # AI helpers (analyze image, treat, translate)
│ │ └─ storage/ # Local history utilities
│ │
│ └─ styles/ # Tailwind/global styles
│
├─ .env.local # API keys (ignored by Git)
├─ next.config.ts
├─ tailwind.config.ts
├─ postcss.config.mjs
└─ README.md

```

---


---

## ⚙️ Setup Instructions

### 1️⃣ Clone Repo
```bash
git clone https://github.com/<your-username>/smart-crop-sentinel.git
cd smart-crop-sentinel

```

### 2️⃣ Install Dependencies
```bash
npm install


```

### 3️⃣ Configure Environment
```bash

Create .env.local:


AI_IMAGE_ANALYSIS_ENDPOINT=...
AI_SOLUTION_RECOMMENDATION_ENDPOINT=...
AI_TRANSLATION_ENDPOINT=...
AI_API_KEY=...


```

###4️⃣ Run Development Server
```bash
npm run dev

```


Visit:
http://localhost:3000

