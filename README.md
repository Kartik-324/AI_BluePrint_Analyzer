# 🏢 CBRE Blueprint Analyzer

## 🎯 Overview

Blueprint Analyzer is an enterprise-grade AI application designed
for analyzing architectural blueprints using advanced AI vision
technologies such as FastAPI, LangChain, OpenAI GPT‑4o Vision, and
Streamlit.

It provides instant, detailed, and conversational analysis of floor
plans and construction documents.


![AI BluePrint Analyzer – Main dashboard and overview](https://github.com/Kartik-324/AI_BluePrint_Analyzer/blob/ba5240b99c1e515a8fc6ed0c02dcd4673e656516/Screenshot%202025-12-11%20141938.png)

![AI BluePrint Analyzer – Blueprint input and analysis setup](https://github.com/Kartik-324/AI_BluePrint_Analyzer/blob/ba5240b99c1e515a8fc6ed0c02dcd4673e656516/Screenshot%202025-12-11%20113655.png)

![AI BluePrint Analyzer – Analysis in progress and results preview](https://github.com/Kartik-324/AI_BluePrint_Analyzer/blob/ba5240b99c1e515a8fc6ed0c02dcd4673e656516/Screenshot%202025-12-11%20113749.png)

![AI BluePrint Analyzer – Final insights and recommendations screen](https://github.com/Kartik-324/AI_BluePrint_Analyzer/blob/ba5240b99c1e515a8fc6ed0c02dcd4673e656516/Screenshot%202025-12-11%20113801.png)


------------------------------------------------------------------------

## 🚀 Key Highlights

-   🤖 **Automatic Blueprint Analysis**
-   💬 **Conversational Q&A**
-   🎤 **Voice Input Support**
-   📐 **Room & Dimension Insights**
-   🏢 **Enterprise-Ready UI**
-   ⚡ **Fast & Accurate (GPT‑4o Vision)**

------------------------------------------------------------------------

## ✨ Features

### 🔍 Automatic Blueprint Analysis

-   Instantly analyzes blueprints
-   Extracts rooms, dimensions, layout, features

### 💬 Conversational Interface

-   Natural language Q&A
-   Context-aware follow‑up questions
-   Pre-built quick questions

### 🎨 Professional UI

-   CBRE-branded styling
-   Split-screen layout (image + chat)
-   Dark mode supported

### 📊 Analysis Capabilities

  Feature               Detects
  --------------------- ----------------------------
  Spatial Analysis      Room counts, locations
  Dimensions            Width, length, total area
  Structural Elements   Walls, doors, windows
  Systems               HVAC, electrical, plumbing
  Accessibility         ADA compliance
  Commercial Features   Parking, common areas

------------------------------------------------------------------------

## 🛠 Technology Stack

### Backend

-   FastAPI\
-   LangChain\
-   OpenAI GPT‑4o\
-   Python 3.9+

### Frontend

-   Streamlit\
-   Custom CSS\
-   Modular architecture

### AI Models

-   GPT‑4o Vision\
-   Whisper (optional)\
-   gTTS fallback

------------------------------------------------------------------------

## 🏗 Architecture

    Streamlit (Frontend)
     ├── Blueprint Viewer (Left)
     └── Chat Interface (Right)
            │
            ▼
    FastAPI (Backend)
     ├── API Endpoints
     ├── AI Processor
     └── Voice Handler
            │
            ▼
    OpenAI Platform (GPT‑4o • Whisper)

------------------------------------------------------------------------

## 📦 Installation

### Prerequisites

-   Python 3.9+
-   OpenAI API Key
-   Git

### Step 1: Clone Repository

``` bash
git clone https://github.com/Kartik-324/CBRE_BluePrint_Analyzer.git
cd BluePrint_Analyzer
```

### Step 2: Setup Virtual Environment

#### Windows

``` bash
python -m venv venv
venv\Scriptsctivate
```

#### Mac/Linux

``` bash
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies

``` bash
pip install -r requirements.txt
```

### Step 4: Add `.env` File

    OPENAI_API_KEY=sk-xxxx
    API_HOST=0.0.0.0
    API_PORT=8000
    STREAMLIT_SERVER_PORT=8501
    OPENAI_MODEL=gpt-4o
    OPENAI_TEMPERATURE=0.3
    OPENAI_MAX_TOKENS=2000

### Step 5: Create Required Directories

``` bash
mkdir uploads backend frontend
```

------------------------------------------------------------------------

## 🚀 Usage

### Option 1: Run Both Services Automatically

Backend:

``` bash
python run_backend.py
```

Frontend:

``` bash
python run_frontend.py
```

### Option 2: Manual Start

Backend:

``` bash
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

Frontend:

``` bash
streamlit run frontend/app.py
```

------------------------------------------------------------------------

## 📖 User Guide

### 1️⃣ Upload Blueprint

Supported formats: JPG, PNG, PDF, GIF, BMP, TIFF

### 2️⃣ Automatic Analysis Provides:

-   Room types & counts\
-   Dimensions\
-   Structural elements\
-   HVAC, plumbing, electrical\
-   Accessibility insights\
-   Circulation & layout analysis

### 3️⃣ Ask Follow-Up Questions

The AI remembers chat context.

### 4️⃣ View Results

-   Zoomable blueprint viewer\
-   Full chat history\
-   Reset with "New Analysis"

------------------------------------------------------------------------

## 📡 API Endpoints

### POST `/api/analyze-blueprint`

Upload blueprint for analysis.

### GET `/`

Health check endpoint.

Visit `/docs` for Swagger UI.

------------------------------------------------------------------------

## 📁 Project Structure

    BluePrint_Analyzer/
     ├── backend/
     │   ├── main.py
     │   ├── ai_processor.py
     │   └── voice_handler.py
     ├── frontend/
     │   ├── app.py
     │   ├── styles.py
     │   └── components.py
     ├── uploads/
     ├── run_backend.py
     ├── run_frontend.py
     ├── requirements.txt
     └── README.md

------------------------------------------------------------------------

## 🧪 Testing

``` bash
curl http://localhost:8000/
curl -X POST http://localhost:8000/api/analyze-blueprint -F "file=@test.jpg"
```

------------------------------------------------------------------------

## 🤝 Contributing

1.  Fork\
2.  Create feature branch\
3.  Commit\
4.  Push\
5.  Create PR

------------------------------------------------------------------------

## 📝 License

MIT License.

------------------------------------------------------------------------

## 📞 Contact

**Developer:** Kartik\
GitHub: `@Kartik-324`

------------------------------------------------------------------------

## 🎯 Roadmap

-   PDF multi‑page support\
-   Batch processing\
-   PDF/Excel export\
-   Authentication\
-   Blueprint comparison\
-   3D visualization

------------------------------------------------------------------------

## ⚠️ Disclaimer

AI-generated results should be verified by licensed professionals.

------------------------------------------------------------------------

## 💡 Tips

-   Use high‑resolution blueprints\
-   Ask clear questions\
-   Verify complex outputs

