# 📄 Intelligent Document Compliance & Process Automation Agent

This project is a modular, AI-powered **document compliance system** built using **LangChain, Google Gemini**, and **Tesseract OCR**. It helps in extracting and analyzing business documents such as invoices, purchase orders, delivery notes, and truck consignments to validate them against compliance rules written in natural language.

---

## 🚀 Features

✅ Upload PDFs (invoice, delivery note, truck consignment)  
✅ OCR (including rotated scanned documents)  
✅ Extract structured data: invoice no, PO no, quantities, prices, vendors  
✅ Apply multi-step **natural language compliance rules**  
✅ Dynamic rule interpretation using **LangChain + Google Gemini**  
✅ Generate structured PASS/FAIL report with explanations  

---

## 🛠 Tech Stack & Why We Chose It

| Tool | Role | Why We Used It |
|------|------|----------------|
| **Python** | Core backend | Robust for AI + text parsing workflows |
| **Tesseract OCR** | Image-to-text | Open-source, accurate text extraction from scanned PDFs |
| **LangChain** | AI agent orchestration | Converts natural language rules into executable Python logic |
| **Google Gemini(gemini-2.0-flash)** | LLM backend | Interprets business rules and dynamically generates validation code |
| **pdf2image** | PDF → Image | Converts PDFs to high-res images for OCR |
| **OpenCV** | Image pre-processing | Detects and corrects rotated document orientation |

---

## 🧠 How It Works (Behind the Scenes)

1. **User uploads** an invoice and delivery-related PDF.
2. PDFs are converted to **images** and run through **OCR with auto-rotation**.
3. Text is parsed to extract structured data (e.g., PO number, dates, quantities).
4. Natural language compliance rules are passed through **LangChain**, which uses **gemini-2.0-flash** to generate Python validation functions.
5. All the rules are batch executed, and results are compiled into a structured **PASS/FAIL report**.

---

## 💻 How to Run the App

### 1. Clone the Repository

git clone https://github.com/Siddarth-11/Compliance_AI_Agent.git

### 2. Set up environment

python -m venv venv
source venv/bin/activate  | On Windows: venv\Scripts\activate

### 3. Install Requirements

pip install -r requirements.txt

**Installation Notes:**

1. Tesseract OCR must be installed separately:

    - Windows: Download from https://github.com/UB-Mannheim/tesseract/wiki
    - Mac: brew install tesseract
    - Linux: sudo apt install tesseract-ocr

### 4. Configure your Google Gemini Api key

Obtain from Google AI Studio
1. Create a .env file.
2. GOOGLE_API_KEY = "your_api_key"

### 5. Run the Notebook ☺️

---

## 🌱 Future Scalability

Here are a few directions this project can evolve in:

1. Use RAG (Retrieval-Augmented Generation) to answer complex questions like:
    "Why did the invoice fail?"
2. Allow uploading **entire document bundles** (zip files) for bulk validation and python function to automatically match documents respectively.
3. Train a ML model to learn compliance rules according to past examples and human auditors to fully automate this process.
4. Integrate with CRM's or ERP's to automatically fetch Invoices and POs and other documents. 
5. Add interactive UI and deploy on the cloud.

**Made with ❤️ using AI, Python, and a passion for automation.**