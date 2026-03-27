# Filtering Coding Instruction Datasets for Quality Checking
### Classification using LLM (ChatGPT-4)

## 📌 Overview
This project leverages **OpenAI's GPT-4** to automate the evaluation of Python coding instruction datasets.  
The system classifies code samples as **High Quality** or **Low Quality** based on predefined criteria such as:
- ✅ Correctness  
- 📖 Clarity & Readability  
- ⚡ Efficiency  
- 🎯 Relevance  

By filtering out low-quality data, the project improves dataset curation for training machine learning models, ensuring more reliable and effective outcomes.

---

## 📂 Dataset
We use the **`python_code_instructions_18k_alpaca`** dataset from Hugging Face, which contains **18,520 samples** of Python instruction-following tasks.  
Each sample includes:
- **Instruction**: Text description of the coding task  
- **Input**: Data structure provided to the code  
- **Output**: Python code generated to solve the task  

---

## ⚙️ Approach
1. **Problem Formulation**  
   - Classification task: High Quality vs. Low Quality  
   - Evaluation criteria: correctness, clarity, efficiency, readability  

2. **Evaluation Method**  
   - Structured prompts guide GPT-4 to assess each sample  
   - Metrics: correctness, clarity, efficiency, relevance  

3. **Implementation**  
   - Preprocessing dataset for structured format  
   - Parallel evaluation using **joblib** for scalability  
   - GPT-4 performs classification based on structured prompts  

---

## 📊 Results
- **Total Samples**: 18,520  
- **High Quality**: 6,991 (37.7%)  
- **Low Quality**: 11,529 (62.3%)  

GPT-4 showed strong performance in identifying correctness and clarity, but struggled with detecting inefficiencies in complex code.

---

## 🔍 Analysis
**Strengths**  
- Reliable classification of correctness and relevance  
- Strong readability and clarity assessment  

**Limitations**  
- Difficulty detecting performance bottlenecks  
- Challenges in runtime behavior evaluation  

**Future Work**  
- Integrating runtime execution for deeper efficiency checks  
- Expanding evaluation criteria for complex/unconventional code  

---

## 📖 References
- Brown et al. (2020). *Language Models are Few-Shot Learners*. [arXiv:2005.14165](https://arxiv.org/abs/2005.14165)  
- Sun et al. (2023). *Text Classification via Large Language Models*. [arXiv:2305.08377](https://arxiv.org/abs/2305.08377)  
- Chae & Davidson (2023). *Large Language Models for Text Classification*. [OSF Preprint](https://doi.org/10.31235/osf.io/sthwk)  

---

## 🚀 Getting Started
### Prerequisites
- Python 3.9+  
- OpenAI API access  
- Hugging Face datasets  

### Installation
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install -r requirements.txt
