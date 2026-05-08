

---

# Main Flow Diagram

```text
                    ┌────────────────────┐
                    │   Candidate Upload │
                    │   Resume (PDF/DOC)│
                    └─────────┬──────────┘
                              │
                              ▼
                 ┌─────────────────────────┐
                 │   Resume Parsing Module │
                 │ (Extract Resume Content)│
                 └─────────┬───────────────┘
                           │
                           ▼
              ┌──────────────────────────────┐
              │ NLP Processing & Preprocessing│
              │ • Tokenization                │
              │ • Stop Word Removal           │
              │ • Lemmatization               │
              │ • POS Tagging                 │
              │ • Named Entity Recognition    │
              └─────────┬────────────────────┘
                        │
                        ▼
              ┌──────────────────────────────┐
              │  Skill & Feature Extraction  │
              │ • Skills                     │
              │ • Education                  │
              │ • Experience                 │
              │ • Certifications             │
              └─────────┬────────────────────┘
                        │
                        ▼
              ┌──────────────────────────────┐
              │ Job Description Processing   │
              │ Recruiter Adds Requirements  │
              └─────────┬────────────────────┘
                        │
                        ▼
              ┌──────────────────────────────┐
              │  BERT / Sentence-BERT Model  │
              │  Generate Semantic Vectors   │
              └─────────┬────────────────────┘
                        │
                        ▼
              ┌──────────────────────────────┐
              │ Cosine Similarity Matching   │
              │ Resume vs Job Description    │
              └─────────┬────────────────────┘
                        │
                        ▼
              ┌──────────────────────────────┐
              │ Candidate Ranking & Scoring  │
              │ • Match Percentage           │
              │ • Resume Strength            │
              └─────────┬────────────────────┘
                        │
                        ▼
              ┌──────────────────────────────┐
              │ Candidate Classification     │
              │ • Fit                        │
              │ • Close Fit                  │
              │ • Not Fit                    │
              └─────────┬────────────────────┘
                        │
                        ▼
              ┌──────────────────────────────┐
              │ Recommendation System        │
              │ • Missing Skills             │
              │ • Resume Improvement Tips    │
              └─────────┬────────────────────┘
                        │
                        ▼
              ┌──────────────────────────────┐
              │ Web Dashboard / HR Panel     │
              │ • Candidate List             │
              │ • Rankings                   │
              │ • Reports                    │
              └──────────────────────────────┘
```

---

# Simple Architecture Diagram

```text
          +--------------------------------+
          |        Recruiter / HR          |
          +---------------+----------------+
                          |
                          v
          +--------------------------------+
          |      Web Application UI        |
          +---------------+----------------+
                          |
                          v
          +--------------------------------+
          |      Resume Upload Module      |
          +---------------+----------------+
                          |
                          v
          +--------------------------------+
          |       NLP Processing Unit      |
          | (NER, POS Tagging, Parsing)    |
          +---------------+----------------+
                          |
                          v
          +--------------------------------+
          | BERT + Cosine Similarity Engine|
          +---------------+----------------+
                          |
                          v
          +--------------------------------+
          |  ML Ranking & Classification   |
          +---------------+----------------+
                          |
                          v
          +--------------------------------+
          |     Database & Dashboard       |
          +--------------------------------+
```

---

# Short Explanation for Presentation

1. Candidate uploads the resume.
2. Resume parser extracts important information.
3. NLP techniques process the resume text.
4. Skills, education, and experience are extracted.
5. Job description is analyzed.
6. BERT/S-BERT converts text into semantic vectors.
7. Cosine similarity compares resume with job description.
8. Machine learning ranks candidates.
9. Candidates are classified as Fit, Close Fit, or Not Fit.
10. The system generates recommendations and displays results on the dashboard.

---

# Best Title for Diagram

## AI-Based Smart Resume Screening and Job Matching System Using NLP and Machine Learning
