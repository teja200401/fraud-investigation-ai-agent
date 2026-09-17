
# Financial Fraud Investigation AI Agent 🔍🤖

An end-to-end automated fraud detection and investigation system combining supervised machine learning, model explainability (SHAP), and an LLM-powered audit agent built with LangChain and Groq.

---

## 🌟 Key Features

* **Imbalanced Data Handling:** Applies **SMOTE** (Synthetic Minority Over-sampling Technique) to address extreme class imbalance in financial transaction datasets.
* **XGBoost Classification:** High-precision machine learning classifier tuned for credit card fraud detection.
* **Explainable AI (SHAP):** Computes exact feature importance contributions for individual transactions to reveal *why* an alert was flagged.
* **Self-Healing LLM Agent:** Powered by **LangChain** and **Groq (`llama-3.3-70b-versatile`)** to convert SHAP feature attributions into readable, natural language forensic audit reports.
* **Secure Key Management:** Implements zero-hardcoding security practices using Google Colab Secrets API.

---

## 🛠️ Tech Stack

| Category | Tools / Libraries |
| :--- | :--- |
| **Language & Env** | Python 3.10+, Google Colab |
| **Machine Learning** | XGBoost, Scikit-Learn, Imbalanced-Learn (SMOTE) |
| **Model Explainability**| SHAP (SHapley Additive exPlanations) |
| **LLM & Orchestration**| LangChain, Groq API (`llama-3.3-70b-versatile`) |
| **Data Processing** | Pandas, NumPy |

---

## 🚀 Getting Started

### 1. Run in Google Colab
Click the badge below to open the notebook directly in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/teja200401/fraud-investigation-ai-agent/blob/main/fraud_investigation_agent.ipynb)

### 2. Configure API Keys
Before running the agent cells, store your Groq API key in Colab:
1. Click the **Secrets** icon (🔑) on the left sidebar in Google Colab.
2. Add a new secret named `GROQ_API_KEY`.
3. Paste your Groq key value and toggle **Notebook access** to ON.

---

## 📊 Pipeline Architecture

1. **Data Preprocessing:** Standardize features and apply SMOTE on training data.
2. **Model Training:** Train an XGBoost model on balanced financial transaction records.
3. **Inference & Explainability:** Generate SHAP values for flagged high-risk transactions.
4. **Agent Investigation:** Pass transaction metadata and SHAP feature weightings to the LangChain/Groq agent to construct a structured forensic summary report.
