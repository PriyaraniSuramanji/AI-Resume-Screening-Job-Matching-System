# AI-Resume-Screening-Job-Matching-System
AI-powered system to automate resume screening and intelligently match candidates with job roles using semantic understan
Problem Statement
With many applicants applying for each position, there has been a decrease in the efficiency of the recruitment process. This is because recruiters have had to go through hundreds, if not thousands, of resumes manually, thus causing inefficiencies and possible bias during the screening process. The end effect is that very talented applicants could be overlooked.

This problem affects:
Recruiters → They are overloaded with work
Firms → They could miss out on the best talents
Applicants → There might not be fairness in the application process

My Understanding of the Problem
Key Issues Identified:
Resumes are difficult to screen
Decisions based on recruiting process could be discriminatory or biased
Why this problem exists:
Too many applications for each available job opening
Absence of intelligent systems to understand resume
My Assumptions:
Need for an effective system to screen resumes quickly
Expectations for unbiased treatment of applicants

Research on Existing Solutions :
Existing Solutions
LinkedIn Job Matcher → Provides recommendations based on keywords
Applicant Tracking System (ATS) → Uses keyword matching to filter applications

Observations and Limitations
Observations:
All current solutions depend greatly on keyword matching
Human intervention is needed

Limitations:
Semantic analysis of the resume not possible
Qualified candidates could get rejected
No proper ranking based on actual relevance

My Identified Gap
The existing solutions do not comprehend the context of the skillset and experience. They base their decision-making process on keyword searches rather than meaning, leading to a skewed candidate assessment.

There  is a need for a system that can:
Read the resume as a human
Match candidates' profiles against jobs smartly
Rank the candidates on the basis of relevance

My Idea
Creating an AI-enabled platform to comprehend resumes by means of language comprehension and matching candidates to job profiles.

My Proposed Approach
The system will process the resume and job profile and filter out key information before matching candidates to a job profile.

Features
Resume parsing and data extraction
Match resume to job description
Rank candidates according to relevance
Dashboard where recruiters can see result

Challenges
Various resume format types
Avoid biases in decisions made by models
Incomplete and inconsistent information in resume

What I Learned
Technical and ethical aspects involved in recruitment process
Lack of context understanding in current systems

Day 3: Research on Existing Solutions
1. Existing Solutions
1. LinkedIn Job Matcher

LinkedIn provides a job matching feature that recommends candidates and job opportunities based on user profiles. It primarily works by analyzing keywords present in resumes and job descriptions. While it is widely used and effective for basic matching, it relies heavily on profile completeness and keyword similarity rather than deep understanding.

2. Applicant Tracking Systems (ATS) – Taleo, Workday

Applicant Tracking Systems are commonly used by organizations to manage large numbers of job applications. These systems automatically filter resumes based on predefined keywords and criteria. They help recruiters save time by eliminating irrelevant applications. However, their filtering mechanism is mostly rule-based and may overlook candidates who do not use exact keywords.

3. HireVue

HireVue is an AI-driven recruitment platform that assists in candidate screening through video interviews and automated assessments. It evaluates candidates based on predefined parameters and behavioral patterns. While it introduces automation and efficiency, its evaluation may not always capture the full context of a candidate’s abilities.

4. Eightfold AI

Eightfold AI is an advanced talent intelligence platform that attempts to go beyond keyword matching by analyzing skills, experience, and career progression. It uses artificial intelligence to provide deeper insights into candidate suitability. Although it improves accuracy compared to traditional systems, it is complex and not easily accessible for smaller organizations.

2. Comparative Analysis

Most of the existing systems aim to reduce the manual effort involved in recruitment. Traditional systems such as ATS and LinkedIn rely mainly on keyword-based filtering, which makes them fast but less accurate. On the other hand, AI-based platforms like HireVue and Eightfold AI attempt to improve the quality of matching by analyzing additional data such as skills and behavior.

Despite these improvements, all systems share a common limitation: they do not fully understand the context of a candidate’s experience. While AI-based systems perform better than traditional ones, they are often more complex and expensive to implement.

3. Limitations

One of the major limitations of current systems is their dependence on keyword matching. Candidates who use different terminology for the same skill may be incorrectly filtered out. Additionally, most systems lack true semantic understanding, meaning they cannot interpret the actual meaning and depth of a candidate’s experience.

Another important concern is bias in AI models. If the training data contains bias, the system may unintentionally favor certain types of candidates. Furthermore, advanced AI systems can be costly and difficult to implement, making them less accessible for smaller companies.

Handling diverse resume formats is also a challenge. Many systems fail to accurately extract information from resumes that do not follow standard structures, leading to incorrect evaluations.

4. Observations

From the analysis, it is clear that most existing solutions focus on improving efficiency rather than accuracy. While automation has reduced the workload for recruiters, it has not completely solved the problem of fair and accurate candidate evaluation.

There is a noticeable gap in systems that can truly understand the context and meaning of a candidate’s profile. This highlights the need for a more intelligent solution that combines efficiency with deeper semantic understanding.


# Flow Diagram for Project Title

# AI-Based Smart Resume Screening and Job Matching System Using NLP and Machine Learning

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
