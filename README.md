# AI-Powered Sybase to Oracle Migration Tool

An intelligent migration solution that leverages Generative AI to automate and optimize database conversion from Sybase to Oracle with accuracy.

## Overview
Migrating enterprise databases from Sybase ASE to Oracle is complex and error-prone. 
This tool uses AI-driven conversion, human-in-the-loop review, and automated testing to ensure fast and reliable migrations.

## Key Features
- Smart Code Conversion: AI-powered transformation of schema objects (tables, views, procedures).
- Interactive Review: Human-in-the-loop editing interface.
- Automated Testing: Pre-migration validation of converted objects.
- Comprehensive Reporting: Detailed analytics and unique migration IDs.
  
## structure

```
sybase-to-oracle-ai/
│
├── app.py                # Main Streamlit application
├── ai_engine/            # AI model and transformation logic
│   ├── model_loader.py   # Loads fine-tuned LLM
│   ├── converter.py      # AI-powered code conversion logic
│   └── tests/            # AI transformation test cases
│
├── db_connectors/        # Database connectivity modules
│   ├── sybase_connector.py
│   ├── oracle_connector.py
│   └── utils.py
│
├── reporting/            # Migration reports & analytics
│   ├── report_generator.py
│   └── logs/
│
├── requirements.txt      # Python dependencies
├── .env                  # Database credentials & AI model path
└── README.md             # Project documentation
```
```
# Flow of work


   ┌─────────────┐        ┌─────────────┐       ┌─────────────┐
   │  Oracle DB  │        │ Sybase DB   │       │   AI Model  │
   └──────┬──────┘        └──────┬──────┘       └──────┬──────┘
          │                       │                   │
          │                       │                   │
   ┌──────▼──────┐       ┌────────▼────────┐   ┌──────▼───────┐
   │  DB Connect │────▶ │ Object Selection│──▶│ AI Conversion│
   └──────┬──────┘       └────────┬────────┘   └──────┬───────┘
          │                        │                  │
          │                        ▼                  │
          │                ┌───────────────┐          │
          │                │ Review & Edit │◀─────────┘
          │                └──────┬────────┘
          │                       ▼
          │                ┌───────────────┐
          │                │   Testing     │
          │                └──────┬────────┘
          │                       ▼
          │                ┌───────────────┐
          └──────────────▶│ Migration &    │
                           │   Reporting   │
                           └───────────────┘

```

# Technical Stack
Frontend: HTML5, Streamlit

Backend: Python 3.8+

AI Engine: Fine-tuned LLM (Transformers)

Database Connectors: Sybase ASE, Oracle CX

## Installation & Setup

1. ** Clone the Repository **
``` bash
git clone https://github.com/your-username/sybase-to-oracle-ai.git
cd sybase-to-oracle-ai
```

**2. Initialize Virtual Environment**
``` bash
python -m venv venv
source venv/bin/activate     # Linux/Mac
venv\Scripts\activate        # Windows 
```

**3. Install Dependencies**
```bash
pip install -r requirements.txt
```

**4. Configure Databases & AI Model**
  

``` 
SYBASE_DSN=your_sybase_connection
ORACLE_DSN=your_oracle_connection
GEMINI_API = REPLACE WITH YOUR API
```

**5. Launch the Application**
``` bash
python app.py
```

## Example Usage
- Login and connect to Sybase & Oracle databases.

- Select schema objects to migrate.

- Review and adjust AI-generated conversions.

- Validate with automated testing.

- Execute migration and download reports.
