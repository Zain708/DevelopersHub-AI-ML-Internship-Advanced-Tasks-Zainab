# DevelopersHub Corporation: AI/ML Engineering Internship Tasks

**Intern:** Zainab  
**Submission Date:** July 2026  
**Due Date:** 14th July, 2026 

## Overview
This repository contains the completed tasks for the AI/ML Engineering Advanced Internship at DevelopersHub Corporation[cite: 1]. As per the requirements, 3 out of the 5 advanced tasks have been completed, focusing on cutting-edge machine learning and artificial intelligence techniques including transformer models, ML pipelines, and LLM applications[cite: 1].

---

## 📂 Task 1: News Topic Classifier Using BERT

### Objective
To fine-tune a pre-trained transformer model (`bert-base-uncased`) to classify news headlines into four distinct topic categories (World, Sports, Business, Sci/Tech) and deploy it for live interaction[cite: 1].

### Methodology / Approach
*   **Dataset:** AG News Dataset (downsampled to 10,000 training and 2,000 testing samples for efficient GPU processing)[cite: 1].
*   **Preprocessing:** Tokenized the combined headline and article text using the Hugging Face `AutoTokenizer`[cite: 1].
*   **Modeling:** Fine-tuned `bert-base-uncased` utilizing the Hugging Face `Trainer` API for 1 epoch on a Tesla T4 GPU[cite: 1].
*   **Deployment:** Built and launched an interactive web interface using Gradio to accept raw text and output predicted categories with confidence scores[cite: 1].

### Key Results & Observations
*   **Performance:** The model achieved an impressive **90.45% Accuracy** and a **90.55% Macro F1-score** after just one epoch of training[cite: 1].
*   **Deployment:** The Gradio web app successfully processed live inputs, demonstrating the viability of lightweight model deployment for NLP classification tasks[cite: 1].

### Live Gradio Deployment Screenshot:
<img width="512" height="209" alt="image" src="https://github.com/user-attachments/assets/d759ac71-67cf-4fea-a68c-ee21aa606e0b" />

---

## 📂 Task 2: End-to-End ML Pipeline with Scikit-learn

### Objective
To build a reusable, production-ready machine learning pipeline for predicting customer churn using the Telco Churn Dataset[cite: 1].

### Methodology / Approach
*   **Data Processing:** Utilized the Scikit-learn `Pipeline` and `ColumnTransformer` APIs to strictly isolate numerical scaling (`StandardScaler`) and categorical encoding (`OneHotEncoder`), preventing data leakage[cite: 1].
*   **Modeling & Tuning:** Trained baseline Logistic Regression and Random Forest models[cite: 1]. Applied `GridSearchCV` to automatically find the optimal hyperparameters for the Random Forest classifier[cite: 1].
*   **Export:** Saved the finalized, winning pipeline into a standalone binary file using `joblib` for future deployment[cite: 1].

### Key Results & Observations
*   **Optimization:** `GridSearchCV` successfully improved the Random Forest model's performance (identifying `max_depth: 10`, `min_samples_split: 5`, `n_estimators: 100`)[cite: 1]. 
*   **Production Readiness:** The entire workflow (imputation, preprocessing, and prediction) is encapsulated in the exported `customer_churn_pipeline.joblib` file, allowing seamless integration into any backend architecture[cite: 1].

### Pipeline Execution and Optimization Screenshot:
<img width="512" height="142" alt="image" src="https://github.com/user-attachments/assets/1ce48861-eb33-4a99-b41c-144f94704b4f" />

---

## 📂 Task 5: Auto Tagging Support Tickets Using LLMs

### Objective
To automatically tag free-text support tickets into specific categories using Large Language Models (LLMs), comparing zero-shot and few-shot learning methodologies[cite: 1].

### Methodology / Approach
*   **Zero-Shot Learning:** Implemented a robust NLI-based zero-shot classifier using the `facebook/bart-large-mnli` model to output the top 3 most probable tags and their confidence percentages[cite: 1].
*   **Few-Shot Learning:** Utilized `google/flan-t5-base` coupled with prompt engineering, providing the model with three explicit in-context examples to guide its text generation toward the desired categorical labels[cite: 1].

### Key Results & Observations
*   **Zero-Shot Efficacy:** The BART model correctly interpreted natural language and accurately assigned probability distributions. For example, it identified a refund request ticket as "Billing & Refunds" with 64.99% confidence and a password error as "Account Access" with 58.24% confidence[cite: 1].
*   **Few-Shot Dynamics:** The FLAN-T5 model successfully generated output based on the prompt template without hallucinating extra words. However, the zero-shot pipeline proved more reliable for strict classification ranking, whereas the few-shot generative approach showed sensitivity to the prompt structure. 
*   **Business Impact:** This pipeline demonstrates how LLMs can instantly route unstructured customer queries, significantly reducing manual triage times[cite: 1].

### Zero-Shot Top 3 Output Screenshot:
<img width="512" height="312" alt="image" src="https://github.com/user-attachments/assets/d58f447b-bff8-4389-9748-5a4bec1d8f9e" />

### Few-Shot Output Screenshot:
<img width="512" height="137" alt="image" src="https://github.com/user-attachments/assets/35d0d1bc-2b60-49a9-9a61-265f42d93553" />



---
