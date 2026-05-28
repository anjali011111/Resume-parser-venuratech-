Resume Parser AI
Project Overview
Resume Parser AI is an intelligent candidate evaluation system built with Python. It automatically parses resumes, detects domain expertise, clusters similar candidates using machine learning, and assigns a weighted score from 0 to 10 to each candidate — helping recruiters identify the best fit efficiently.
This project was developed as part of the Venura Tech AI-Python Internship Program.

Problem Statement
Recruiters spend enormous time manually skimming hundreds of resumes. Most automated systems rely on simple keyword matching, which fails to understand context. This project builds a smarter system that:

Understands the context of skills (not just keywords)
Groups candidates into skill clusters using ML
Assigns a fair, multi-dimensional score to every candidate
Visualizes results in a professional dashboard


Features
FeatureDescriptionNLP PreprocessingCustom tokenizer, stopword removal, stemmer (pure Python)Domain DetectionMatches resumes to 6 domains using skill knowledge baseAchievement ScoringDetects action verbs vs weak signalsTF-IDF VectorizationConverts resume text into numerical feature vectorsK-Means ClusteringGroups candidates by skill similarityPCA Visualization2D cluster plot using dimensionality reductionCosine SimilarityResume-to-resume similarity heatmapWeighted ScoringFinal score (0–10) from 5 dimensionsDashboard8-panel matplotlib visualizationCSV ExportSaves all scores to a spreadsheet

Tech Stack

Language: Python 3.12
NLP: Custom-built (no NLTK dependency)
ML: scikit-learn (TF-IDF, K-Means, PCA, Cosine Similarity)
Data: pandas, numpy, scipy
Visualization: matplotlib, seaborn


Project Structure
resume_parser_project/
│
├── src/
│   └── resume_parser.py       # Main source code
│
├── output/
│   ├── resume_parser_dashboard.png   # Generated visual dashboard
│   └── resume_scores.csv             # Scored candidates spreadsheet
│
├── docs/
│   └── project_report.pdf     # Project report (submit with project)
│
├── requirements.txt            # Python dependencies
└── README.md                   # This file

How to Run
Step 1 — Clone the repository
bashgit clone https://github.com/YOUR_USERNAME/resume-parser-ai.git
cd resume-parser-ai
Step 2 — Install dependencies
bashpip install -r requirements.txt
Step 3 — Run the parser
bashpython src/resume_parser.py
Step 4 — View outputs

Terminal: Candidate scores and grades printed
output/resume_parser_dashboard.png — Visual dashboard
output/resume_scores.csv — Scores spreadsheet


Scoring System
Each resume is scored out of 10 using 5 weighted dimensions:
DimensionWeightWhat it measuresDomain Match35%How well skills align with the detected fieldAchievement Signals25%Action verbs (led, built, reduced) vs weak wordsEducation15%Degree, institution, GPA keywordsResume Detail10%Depth and length of the resumeSkill Breadth15%Range of technical competencies
Grade Scale:

8.0 – 10.0 → EXCEPTIONAL
6.5 – 7.9  → STRONG
5.0 – 6.4  → MODERATE
3.0 – 4.9  → WEAK
0.0 – 2.9  → NOT RECOMMENDED


Dashboard Panels

Candidate Leaderboard — Ranked horizontal bar chart
Grade Distribution — Donut chart of candidate grades
Top 3 Score Profile — Radar/spider chart of score dimensions
K-Means Skill Clusters — PCA scatter plot of ML clusters
Resume Similarity Matrix — Cosine similarity heatmap
Domain Distribution — Bar chart of detected domains
Score vs Detail Depth — Scatter plot with trend line
Score Breakdown — Stacked bar by component


Sample Output
*** Ravi Kumar         Score: 6.0/10  [MODERATE]
    Domain    : DevOps / Cloud         Job: DevOps Engineer
    Skills    : devops, aws, terraform, docker, kubernetes, helm
    Strengths : architected, implemented, reduced, built, managed

**  Aditya Menon       Score: 5.9/10  [MODERATE]
    Domain    : Software Engineering   Job: Full Stack Engineer
    Skills    : python, react, fastapi, graphql, docker, typescript
    Strengths : built, designed, optimized, implemented, deployed

Future Improvements

Integrate actual Kaggle Resume Dataset (CSV ingestion)
Add BERT/Word2Vec embeddings for semantic similarity
Build a web UI using Flask or Streamlit
Support PDF resume parsing (PyMuPDF)
Add job description matching score


Author
R SAI CHANDRIKANJALI
Venura Tech AI-Python Internship Program
Batch: 2026
GitHub: https://github.com/anjali011111/Resume-parser-venuratech-


License
This project is submitted as part of an internship program. Educational use only.
