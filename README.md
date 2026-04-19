# 🤖 AI Resume Screening & Skill Matching System

An NLP-powered system that automates resume screening by matching skills, computing semantic similarity, ranking candidates, and delivering explainable insights — helping recruiters make faster, smarter hiring decisions.

---

## 📌 Problem Statement

Recruiters often receive hundreds of resumes for a single job role. Manually reviewing each one is time-consuming, inconsistent, and error-prone.

This project automates the screening process by:
- Extracting and matching skills between a resume and a job description
- Computing semantic similarity scores using TF-IDF and cosine similarity
- Ranking multiple candidates based on their relevance scores
- Generating explainable insights: strengths, gaps, and recommendations

---

## 🚀 Features

| Feature | Description |
|---|---|
| **Skill Extraction** | Identifies key skills from both resume and job description |
| **Skill Matching** | Finds matched and missing skills with a basic match score |
| **Semantic Similarity** | Uses TF-IDF + cosine similarity for deeper text comparison |
| **Resume Ranking** | Ranks multiple candidates from highest to lowest match |
| **PDF Resume Support** | Parses and processes real uploaded PDF resumes |
| **Explainable AI** | Highlights top matching keywords driving the similarity score |
| **Candidate Summary** | Outputs strengths, skill gaps, and a recruiter recommendation |
| **Visualization** | Bar chart comparing match scores across candidates |

---

## 🛠️ Tech Stack

- **Language:** Python
- **Libraries:** `pandas`, `numpy`, `matplotlib`, `scikit-learn`, `PyPDF2`, `re`
- **NLP Techniques:** TF-IDF Vectorization, Cosine Similarity, Keyword Matching
- **Environment:** Google Colab / Jupyter Notebook

---

## 📁 Project Structure

```
ai-resume-screening/
│
├── resume_screening.ipynb   # Main notebook with all steps
├── README.md                # Project documentation
└── sample_resume.pdf        # (Optional) Sample PDF resume for testing
```

---

## ⚙️ How It Works

### Step 1 — Input Data
Define a job description and one or more resume texts as inputs.

### Step 2 — Text Preprocessing
Clean and normalize text: lowercase, remove punctuation, strip extra whitespace.

### Step 3 — Skill Extraction
Match text against a predefined skills list to identify required and present skills.

### Step 4 — Skill Matching
Compute a **match score** based on the overlap between job-required and resume skills.

```
Match Score = (Matched Skills / Total Required Skills) × 100
```

### Step 5 — Semantic Similarity (TF-IDF)
Convert texts to TF-IDF vectors and compute **cosine similarity** to capture broader contextual relevance beyond exact keywords.

### Step 6 — Resume Ranking
Score and rank multiple resumes against the same job description.

### Step 7 — Visualization
Generate a bar chart comparing match scores across all candidates.

### Step 8 — Explainable AI (Keyword Insights)
Extract the top overlapping TF-IDF keywords to explain why a resume matched.

### Step 9 — PDF Resume Input
Upload and parse a real PDF resume using `PyPDF2`, then run it through the full pipeline.

### Step 10 — Candidate Evaluation Summary
Output a human-readable summary with:
- Match score
- Matched skills (Strengths)
- Missing skills (Gaps)
- Recommendation: ✅ Strong Fit / ⚠️ Moderate Fit / ❌ Low Fit

---

## 📊 Sample Output

```
------ AI Resume Screening Result ------

Matched Skills: ['python', 'machine learning', 'pandas', 'numpy', 'nlp', 'data analysis']
Missing Skills: ['sql', 'data visualization']
Resume Match Score: 75.0%

------ Candidate Evaluation Summary ------

Strengths:
- Strong in python
- Strong in machine learning
- Strong in pandas

Gaps:
- Missing sql
- Missing data visualization

Recommendation: ⚠️ Moderate Fit (Needs Improvement)
```

---

## 🔧 Setup & Usage

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/ai-resume-screening.git
cd ai-resume-screening
```

### 2. Install Dependencies
```bash
pip install scikit-learn pandas numpy matplotlib PyPDF2
```

### 3. Run the Notebook
Open `resume_screening.ipynb` in **Jupyter Notebook** or **Google Colab** and run cells sequentially.

### 4. Upload a PDF Resume (Optional)
Use the file upload cell in Step 9 to test with a real resume PDF.

---

## 📈 Future Improvements

- Integrate **BERT / Sentence Transformers** for deeper semantic understanding
- Build a web interface using **Streamlit** or **Flask**
- Support multi-language resumes
- Add a database to store and compare candidate profiles over time
- Fine-tune skill extraction with a domain-specific NER model

---

## 🙋 Author

**Shree Kiran**  
Data Science Intern | AI/ML Enthusiast  
📧 srshreekiran2002@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/shree-kiran-ab0a96244) | [GitHub](https://github.com/kiran08012002)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
