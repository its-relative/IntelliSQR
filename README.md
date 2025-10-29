# 🧾 PAN–Entity Extraction using Hugging Face LLM

This project extracts **PAN–Entity relationships** from SEBI PDF documents using a **Hugging Face LLM (Mistral-7B-Instruct)**.  
It converts unstructured regulatory text into a clean, tabular format of triples:

<PAN>, PAN_Of, <Entity>

---

## 🚀 Workflow
1. **PDF Parsing** → Extracts text from SEBI order PDFs using `PyMuPDF`.
2. **Text Cleaning** → Preprocesses and segments the extracted text for model input.
3. **LLM Inference** → Uses the `Mistral-7B-Instruct` model (via Hugging Face Transformers) to generate structured triples.
4. **Parsing & Validation** → Filters and validates model output using regex and logical checks.
5. **CSV Export** → Saves the final structured results into `pan_relations_filtered.csv`.

---

## 📊 Example Output
After cleaning and validation, the model produced **68 accurate PAN–Entity pairs**, such as:

| PAN         | Relation | Entity Name                                  |
|--------------|-----------|---------------------------------------------|
| AAACM9185B   | PAN_Of    | MAHESHWARI FINANCIAL SERVICES PVT. LTD.     |
| AADCE0088L   | PAN_Of    | ECOSPACE INFOTECH PVT. LTD.                 |
| AAPPG1345M   | PAN_Of    | SANJEEV GOEL                                |

---

## 🧠 Key Concept
Large Language Models (LLMs) can be leveraged to extract **structured data** (entities, relationships, etc.) from **unstructured regulatory or financial documents**.  
This allows scalable automation for **compliance analytics, data curation, and pipeline integration**.

---

## 🧰 Technologies Used
- 🐍 **Python**
- 📚 **Hugging Face Transformers**
- 🧩 **PyMuPDF**
- 🧮 **Pandas**
- 🔍 **Regex**

---

## 📁 Output Files
- `pan_relations_filtered.csv` → Contains final valid PAN–Entity mappings  
- Intermediate files: model responses, raw extracted text, and filtered outputs

---

## 🔧 Future Improvements
- Automate correction of invalid or incomplete entries  
- Extend extraction to multiple relationship types  
- Integrate with **ETL pipelines** or **NoSQL databases** for production use  
- Experiment with **fine-tuning smaller LLMs** for faster inference

---

✅ *Built with Hugging Face and Python for intelligent regulatory data extraction.*
