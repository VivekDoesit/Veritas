<div align="center">

# ◉ VERITAS

### See the evidence. Understand the claim.

**Evidence-grounded AI fact checking & bias detection.**

[![Built with React](https://img.shields.io/badge/Frontend-React%20%2B%20Vite-61DAFB?style=for-the-badge&logo=react&logoColor=white)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/Language-TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Claude](https://img.shields.io/badge/AI-Claude-CC785C?style=for-the-badge)](https://www.anthropic.com/)
[![SerpApi](https://img.shields.io/badge/Search-SerpApi-4285F4?style=for-the-badge)](https://serpapi.com/)

<br />

> **Don't just ask AI what is true. Show me the evidence.**

</div>

---

## 🧭 What is Veritas?

**Veritas** is an evidence-grounded AI fact-checking and bias-detection platform designed to help people understand claims, headlines, and statements through **retrieved evidence rather than AI-generated assumptions**.

Instead of simply asking an AI:

> *"Is this true?"*

Veritas follows an evidence-first pipeline:

```text
Claim
  ↓
Claim Analysis
  ↓
Search the Web
  ↓
Collect Multiple Sources
  ↓
Compare Supporting & Contradicting Evidence
  ↓
Claude Analysis
  ↓
Bias & Framing Detection
  ↓
Explainable Verdict
  ↓
Source Trail
````

The goal is simple:

### **Make evidence visible.**

---

# 🎯 The Problem

The internet has never made information more accessible.

But it has also made it increasingly difficult to distinguish between:

* facts
* opinions
* misleading claims
* emotionally loaded statements
* incomplete information
* sensational headlines
* outdated information
* conflicting evidence
* AI-generated misinformation

Traditional search engines provide links.

AI chatbots provide answers.

But users often don't get a clear picture of:

> **What evidence supports this claim, what contradicts it, and how is the statement being framed?**

That's where Veritas comes in.

---

# 💡 The Solution

Veritas combines **real-time web search + evidence aggregation + Claude-powered analysis** to create an explainable fact-checking workflow.

Rather than treating AI as an oracle, Veritas treats AI as an **evidence analyst**.

### Veritas asks:

> What does the claim actually say?

> What evidence exists?

> Which sources support it?

> Which sources contradict it?

> Where is the evidence uncertain?

> Is the statement using loaded or sensational language?

> What is fact, and what is framing?

---

# ✨ Core Features

## 🔎 Evidence-Grounded Fact Checking

Submit a claim and Veritas searches the web for relevant evidence.

It can retrieve information from:

* General web search
* News sources
* Academic-oriented searches
* Institutional sources
* Government sources
* Other publicly indexed sources

---

## ⚖️ Evidence Comparison

Veritas doesn't stop after finding one matching result.

It searches for multiple perspectives and organizes evidence into:

### 🟢 Supports

Evidence that supports the claim.

### 🔴 Contradicts

Evidence that conflicts with the claim.

### ⚪ Context / Mixed

Evidence that adds nuance, limitations, or doesn't clearly fall into either category.

---

## 🧠 Explainable AI Analysis

Claude analyzes the retrieved evidence and produces a structured assessment.

Instead of:

> ❌ TRUE

or

> ❌ FALSE

Veritas can classify a claim as:

| Verdict                     | Meaning                                                                          |
| --------------------------- | -------------------------------------------------------------------------------- |
| 🟢 **Supported**            | Available evidence generally supports the claim                                  |
| 🟡 **Partially Supported**  | Some parts are supported, but the claim is broader or stronger than the evidence |
| 🔴 **Contradicted**         | Available evidence conflicts with the claim                                      |
| ⚪ **Insufficient Evidence** | Available evidence isn't enough to make a reliable determination                 |
| 🔵 **Opinion**              | The statement is primarily subjective or value-based                             |
| 🟣 **Mixed**                | Evidence is substantially conflicting or context-dependent                       |

---

# 📊 Evidence Strength

Veritas provides an **Evidence Strength** assessment based on the retrieved evidence.

Example:

```text
Evidence Strength

████████░░ 78 / 100
```

### Important:

This is **not a probability that the claim is true**.

It represents an AI-assisted assessment of factors such as:

* relevance of retrieved evidence
* agreement between sources
* strength of available evidence
* contradictions
* limitations
* consistency

Veritas intentionally avoids presenting this as mathematical certainty.

---

# 📰 Source Transparency

Every important conclusion is connected to the evidence that influenced it.

Each source can display:

```text
Source
Title
Domain
Publication Date
Source Type
Evidence Role
Relevant Snippet
Why It Matters
External Link
```

Users can follow the original source and independently inspect it.

### The principle:

> **Don't trust the AI. Inspect the evidence.**

---

# 🧩 Claim Classification

Before attempting to determine a verdict, Veritas analyzes what kind of statement it received.

Possible classifications include:

```text
FACTUAL
OPINION
PREDICTION
QUESTION
MIXED
NOT FACT-CHECKABLE
```

This prevents the system from pretending that subjective statements have objective answers.

For example:

> "Chocolate ice cream is the best."

Veritas shouldn't attempt to prove that objectively.

It should recognize that the statement expresses an opinion.

---

# 🕵️ Bias & Language Detection

Veritas analyzes the **language and framing** of a claim.

It can identify patterns such as:

* Loaded language
* Emotional language
* Sensationalism
* Absolute statements
* Sweeping generalizations
* False certainty
* Ad hominem language
* Fear-based framing
* Overgeneralization
* Potentially misleading framing

### Example

Input:

> "The government finally admitted its disastrous economic policy failed."

Veritas may identify:

```text
FACTUAL COMPONENT
"The government admitted..."

LOADED LANGUAGE
"disastrous"

FRAMING
"finally admitted"

CLAIM
"economic policy failed"
```

The system does **not** simply label the entire statement as "biased."

Instead, it explains **which language creates the framing and why**.

---

# 📰 Headline Comparison

Veritas can compare two headlines covering the same event.

For example:

### Headline A

> "Scientists discover miracle cancer cure."

### Headline B

> "Early-stage study identifies promising cancer treatment."

The system can highlight:

* emotional language
* certainty
* sensationalism
* loaded terms
* framing differences
* shared factual elements

The goal isn't to declare a winner.

The goal is to make the **difference in framing visible**.

---

# 🏗️ Architecture

```text
                         ┌─────────────────────┐
                         │       VERITAS       │
                         │    React Frontend   │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │     Express API     │
                         │   Backend / Server  │
                         └──────────┬──────────┘
                                    │
                   ┌────────────────┼────────────────┐
                   │                │                │
                   ▼                ▼                ▼
             ┌──────────┐     ┌──────────┐    ┌────────────┐
             │ SerpApi  │     │  Claude  │    │ Validation │
             │  Search  │     │   AI     │    │   + Zod    │
             └────┬─────┘     └────┬─────┘    └────────────┘
                  │                │
                  ▼                ▼
             Web Evidence     AI Analysis
                  │                │
                  └───────┬────────┘
                          ▼
                  ┌───────────────┐
                  │   Evidence    │
                  │   Synthesis   │
                  └───────┬───────┘
                          │
                          ▼
                  ┌───────────────┐
                  │    Veritas    │
                  │    Verdict    │
                  └───────────────┘
```

---

# 🔄 Verification Pipeline

## 01 — Submit

The user submits a claim, headline, or statement.

```text
"Electric vehicles are worse for the environment
than petrol cars."
```

---

## 02 — Understand

Veritas analyzes the claim and determines its type.

```text
Claim Type → Factual
```

---

## 03 — Generate Queries

Multiple search queries are generated to avoid relying on one search result.

Example:

```text
electric vehicles environmental impact

electric vehicles vs petrol environmental impact

electric vehicle lifecycle emissions

electric vehicle environmental impact research

electric vehicle environmental impact contradictory evidence
```

---

## 04 — Search

SerpApi retrieves relevant search results.

```text
Google Search
Google News
Academic-oriented Search
```

---

## 05 — Build Evidence Pool

Results are:

* normalized
* deduplicated
* categorized
* linked to source IDs

---

## 06 — Analyze

Claude receives the claim and retrieved evidence.

It analyzes:

* supporting evidence
* contradictory evidence
* context
* uncertainty
* causal relationships
* unsupported conclusions
* framing
* language

---

## 07 — Generate Verdict

The system creates a structured result.

```text
Verdict
Summary
Evidence Strength
Supporting Sources
Contradicting Sources
Uncertainties
Bias Analysis
Fact vs Framing
```

---

## 08 — Show the Evidence

The user receives an explainable report with links to the original sources.

---

# 🧠 Why Claude?

Claude is used as the **reasoning and evidence-synthesis layer**.

Veritas does not ask Claude to independently decide what is true.

Instead, Claude receives:

```text
USER CLAIM
+
RETRIEVED EVIDENCE
+
SOURCE METADATA
```

and analyzes the relationship between them.

This creates an important distinction:

```text
Traditional AI

Question
   ↓
AI
   ↓
Answer


Veritas

Claim
   ↓
Web Search
   ↓
Evidence
   ↓
Comparison
   ↓
AI Analysis
   ↓
Explainable Result
   ↓
Source Trail
```

---

# 🔍 Why SerpApi?

SerpApi provides structured access to search-engine results without requiring Veritas to manually scrape search engines.

It allows the application to retrieve relevant:

* search results
* news results
* snippets
* URLs
* domains
* metadata

This makes SerpApi the **evidence retrieval layer** of Veritas.

---

# 🛡️ Anti-Hallucination Design

Veritas is designed around an evidence-grounded AI workflow.

Claude is instructed to:

* never invent citations
* never invent URLs
* never invent quotations
* never invent statistics
* never invent publication dates
* never claim a source says something it doesn't
* acknowledge insufficient evidence
* acknowledge conflicting sources
* distinguish correlation from causation
* distinguish absence of evidence from evidence of absence

Search snippets are treated as **evidence leads**, not as perfect substitutes for reading the full source.

---

# 🔐 Security

API keys are never exposed to the frontend.

Sensitive credentials are stored using environment variables:

```env
SERPAPI_KEY=
ANTHROPIC_API_KEY=
CLAUDE_MODEL=
```

The backend implements security measures including:

* Helmet
* CORS
* Rate limiting
* Request validation
* Environment variables
* Request size limits
* Centralized error handling

### Never commit `.env`

The repository includes:

```text
.env.example
```

but not actual secrets.

---

# 🎨 Design System

Veritas uses a warm editorial technology aesthetic.

### Primary Palette

| Color      | Hex       | Purpose                      |
| ---------- | --------- | ---------------------------- |
| Coral      | `#E7717D` | Primary actions / brand      |
| Cool Gray  | `#C2CAD0` | Secondary surfaces           |
| Warm Beige | `#C2B9B0` | Main backgrounds             |
| Deep Brown | `#7E685A` | Typography / dark surfaces   |
| Lime       | `#AFD275` | Supporting / positive states |

The visual language combines:

**Investigative journalism × Premium technology × Editorial design**

---

# 🛠️ Tech Stack

### Frontend

* React
* Vite
* TypeScript
* Tailwind CSS
* Framer Motion
* Lucide React

### Backend

* Node.js
* Express
* TypeScript
* Zod
* Helmet
* CORS
* Express Rate Limit

### AI

* Anthropic Claude API

### Search

* SerpApi

---

# 📁 Project Structure

```text
veritas/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── hooks/
│   │   ├── lib/
│   │   ├── types/
│   │   ├── data/
│   │   ├── animations/
│   │   ├── App.tsx
│   │   └── main.tsx
│   │
│   ├── public/
│   ├── package.json
│   └── vite.config.ts
│
├── backend/
│   ├── src/
│   │   ├── routes/
│   │   ├── controllers/
│   │   ├── services/
│   │   ├── middleware/
│   │   ├── schemas/
│   │   ├── types/
│   │   ├── utils/
│   │   ├── config/
│   │   └── server.ts
│   │
│   └── package.json
│
├── .env.example
├── .gitignore
├── package.json
└── README.md
```

---

# 🚀 Getting Started

## Prerequisites

Make sure you have installed:

* Node.js 18+
* npm
* Git

You will also need:

* A [SerpApi](https://serpapi.com/) API key
* An [Anthropic](https://console.anthropic.com/) API key

---

## 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/veritas.git

cd veritas
```

---

## 2. Configure environment variables

Create:

```text
backend/.env
```

Add:

```env
SERPAPI_KEY=your_serpapi_key
ANTHROPIC_API_KEY=your_anthropic_key
CLAUDE_MODEL=your_claude_model
PORT=5000
FRONTEND_URL=http://localhost:5173
```

Never commit this file.

---

# ▶️ Running Locally

## Start Backend

```bash
cd backend

npm install

npm run dev
```

Backend:

```text
http://localhost:5000
```

---

## Start Frontend

Open another terminal:

```bash
cd frontend

npm install

npm run dev
```

Frontend:

```text
http://localhost:5173
```

---

# 🧪 Demo Mode

Veritas includes a demo mode for hackathon presentations.

When enabled, the application can demonstrate the complete UI and analysis experience using clearly labeled sample data.

Demo results are explicitly marked:

```text
DEMO MODE — SAMPLE EVIDENCE
```

Live API results are labeled:

```text
LIVE VERIFICATION
```

This prevents demo data from being mistaken for real-time evidence.

---

# 🌐 Deployment

The frontend and backend are intentionally separated.

### Frontend

Can be deployed using:

* Vercel
* GitHub Pages
* Netlify
* Other static hosting

### Backend

Can be deployed using:

* Render
* Railway
* Fly.io
* Other Node.js-compatible platforms

### Important

GitHub Pages cannot securely run the Express backend or store private API credentials.

Therefore API keys should always remain on the backend.

---

# 🔑 API Endpoints

## Health Check

```http
GET /api/health
```

---

## Verify Claim

```http
POST /api/verify
```

Request:

```json
{
  "claim": "Coffee causes dehydration."
}
```

---

## Compare Headlines

```http
POST /api/compare-headlines
```

Request:

```json
{
  "headlineA": "Scientists discover miracle cure.",
  "headlineB": "Early-stage study identifies promising treatment."
}
```

---

# 📸 Product Flow

```text
┌─────────────────────┐
│   Submit a Claim    │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│   Analyze Claim     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│   Search the Web    │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Collect Evidence    │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Compare Sources     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Claude Analysis     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Bias + Framing      │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Explainable Verdict │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│   Source Trail      │
└─────────────────────┘
```

---

# ⚠️ Limitations

Veritas is an AI-assisted evidence analysis system.

It is not an absolute authority.

Potential limitations include:

* Search engine coverage
* Source availability
* Search snippets lacking full context
* Conflicting research
* Outdated sources
* Low-quality sources
* AI interpretation errors
* Ambiguous claims
* Rapidly changing information

For this reason, Veritas emphasizes:

> **Evidence transparency over artificial certainty.**

---

# 🔮 Future Roadmap

Potential future improvements include:

### 🌐 Browser Extension

Check claims while browsing the web.

### 📰 Article Analysis

Paste an entire article and receive:

* claim extraction
* evidence mapping
* bias analysis
* source verification

### 📱 Mobile Application

Native mobile experience for rapid claim verification.

### 📚 Source Reliability Profiles

Provide additional context about source history and transparency without reducing credibility to a simplistic score.

### 🧬 Claim Graphs

Visualize relationships between:

```text
Claim
 ↓
Subclaims
 ↓
Evidence
 ↓
Sources
```

### 🗂️ Verification History

Allow users to save previous investigations.

### 🌍 Multilingual Verification

Support claims in multiple languages.

### 🧠 Retrieval Improvements

Add more specialized databases and retrieval sources.

---

# 🏆 Hackathon Vision

Veritas was built around a simple idea:

> **The future of fact checking shouldn't be about asking an AI for a verdict.**

It should be about giving people:

**Evidence.**

**Context.**

**Transparency.**

**Agency.**

Veritas doesn't ask users to blindly trust an algorithm.

It helps them investigate.

---

<div align="center">

## VERITAS

### Search. Compare. Understand.

**Don't just ask AI what is true.
Show me the evidence.**

<br />

Built with ❤️ using React, Node.js, SerpApi.

</div>
