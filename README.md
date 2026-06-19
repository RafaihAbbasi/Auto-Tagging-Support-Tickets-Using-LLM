# Auto-Tagging Customer Support Tickets Using LLMs

An automated support ticket classification system built using the **Gemini 2.5 Flash** model. This project automates the process of reading customer complaints and assigning relevant category tags, comparing the performance of **Zero-Shot** and **Few-Shot** prompting techniques.

---

## 📌 Project Overview
In a production environment, analyzing thousands of customer support tickets manually is time-consuming. This project solves that problem by using a Large Language Model (LLM) to automatically categorize incoming tickets into structured tags (e.g., `Account Access`, `Technical Issue`, `Feature Request`).

The project demonstrates how structure-constrained prompts and **Few-Shot Learning** significantly improve the classification accuracy and reliability of LLMs compared to **Zero-Shot Learning**.

---

## 🛠️ Tech Stack & Tools
* **Language:** Python
* **LLM Engine:** Google Gemini API (`gemini-2.5-flash`)
* **Environment:** Google Colab / Jupyter Notebook
* **Libraries:** `google-genai`, `pandas`, `scikit-learn`, `json`

---

## 🚀 Key Features & Implementation
* **Data Ingestion & Cleaning:** Reads raw support tickets and structures them into a clean Pandas DataFrame.
* **Structured JSON Outputs:** Prompts are engineered to strictly force the LLM to return valid JSON arrays containing exactly 3 tags per ticket.
* **Prompting Strategy Comparison:**
  * **Zero-Shot Prompting:** Evaluating the model's performance without giving prior examples.
  * **Few-Shot Prompting:** Guiding the model with high-quality, structured examples to stabilize formatting and increase accuracy.
* **Evaluation Pipeline:** Generates classification reports (Accuracy, Precision, Recall, F1-Score) to mathematically evaluate the results.

---

## 📈 Evaluation & Results
Both methods were tested on the dataset, yielding the following insights:
* **Primary Tag Accuracy:** Achieved **70.0%** accuracy on both models.
* **Formatting Reliability:** The **Zero-Shot** model occasionally failed to comply with the strict JSON criteria, resulting in a parsing `Error`. 
* **Few-Shot Superiority:** The **Few-Shot** approach achieved perfect compliance (0% format errors) and recorded a **1.00 Recall/F1-Score** on critical classes like *Account Access* and *Feature Request*, proving its reliability for production pipelines.

---

## ⚙️ How to Run This Project

1. **Clone the repository:**
```bash
   git clone [https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY_NAME.git](https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY_NAME.git)
