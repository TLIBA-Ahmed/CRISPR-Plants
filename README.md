# 🌿 CRISPR Plants AI – sgRNA Design & Prediction with Machine Learning

This project explores the use of **Artificial Intelligence and Machine Learning for CRISPR guide RNA design in plants** using real genomic data from the Ensembl Plants API.

The notebook demonstrates a **complete experimental pipeline** combining:
- genomic data retrieval
- sgRNA candidate generation
- deep learning efficiency prediction
- off-target analysis
- machine learning model comparison
- an LLM-based CRISPR design pipeline

---

# 📊 Project Overview

Genome editing with **CRISPR-Cas systems** requires selecting efficient and safe guide RNAs (sgRNAs).  
This notebook implements an **AI-assisted pipeline** to identify optimal guides for important plant genes.

The workflow includes:

1️⃣ Retrieval of genomic sequences from **Ensembl Plants REST API**  
2️⃣ sgRNA candidate generation for **Cas9 and Cas12a**  
3️⃣ Efficiency prediction using deep learning models  
4️⃣ Off-target risk estimation  
5️⃣ Machine learning model comparison  
6️⃣ Simulation of an **LLM-based CRISPR design agent**

---

# 🌱 Target Plant Species

The project analyzes agriculturally important genes from four plant species:

| Species | Gene | Biological Role |
|------|------|------|
| Arabidopsis thaliana | FT (AT1G65480) | Flowering regulation |
| Oryza sativa | GS3 | Rice grain size |
| Zea mays | VGT1 | Flowering time in maize |
| Triticum aestivum | TaGW2 | Wheat grain weight |

These genes are widely studied in **plant genetics and crop improvement**.

---

# ⚙️ Technologies Used

### Programming
- Python
- Jupyter Notebook

### Data Science
- numpy  
- pandas  
- scikit-learn  

### Visualization
- matplotlib  
- seaborn  

### Bioinformatics
- Ensembl Plants REST API

### AI Models Simulated
- DeepCas9
- DeepCpf1
- CRISPR-ONT
- CRISPR-OFFT
- Random Forest
- Gradient Boosting

---

# 🔬 Pipeline Architecture

The notebook follows this pipeline:

Genomic Data (Ensembl API)
↓
Sequence Processing
↓
PAM Site Detection
↓
sgRNA Candidate Generation
↓
Efficiency Prediction
(DeepCas9 / DeepCpf1)
↓
Attention-based Analysis
(CRISPR-ONT)
↓
Off-target Risk Prediction
(CRISPR-OFFT)
↓
ML Model Comparison
↓
Final Ranking of sgRNA Guides


---

# 🤖 CRISPR-GPT Simulation

The project also simulates a **CRISPR design assistant powered by LLM agents**.

In a production environment, each step of the pipeline could call a large language model to:

- analyze gene sequences
- propose sgRNA designs
- evaluate editing risks
- generate experimental reports

Example concept:

```python
response = openai.chat.completions.create(
    model="gpt-4o",
    messages=[
        {"role": "system", "content": "You are CRISPR-GPT, an expert in plant genome editing."},
        {"role": "user", "content": "Design sgRNAs for a plant gene."}
    ]
)

