# JobGenie AI

**AI-Powered Career Assistant for Smarter Job Applications**

---

## 🧠 Overview

JobGenie AI is a smart job application assistant that uses state-of-the-art NLP models to:

* Extract key requirements from job listings
* Match resumes semantically to job posts
* Generate personalized cover letters
* Prepare users with job-specific mock interview questions

Built with Spring Boot (backend), Angular (frontend), and Hugging Face models for NLP, it is a complete solution for job seekers to stand out.

---

## 💡 Key Features

* 🔍 Live job listing ingestion from Adzuna, Remotive, and USAJobs APIs
* 🧾 Resume parsing and skill extraction from PDF or text
* 🧠 AI-powered job summarization and requirement extraction (NER)
* 🤝 Resume-job matching with semantic similarity using embeddings
* 📝 Personalized AI-generated cover letters
* 🎤 Job-specific mock interview question generator
* 📊 Dashboard with match scores and application analytics

---

## 🧰 Tech Stack

**Backend:**

* Spring Boot
* PostgreSQL
* Redis or FAISS for vector similarity
* Hugging Face Transformers (via local models or Inference API)

**Frontend:**

* Angular 17
* Tailwind CSS / Angular Material

**Infrastructure:**

* Docker
* GitHub Actions CI/CD
* Deployed on Railway / Vercel / Render

---

## 🧠 Hugging Face Models Used

| Task                     | Model                                                          |
| ------------------------ | -------------------------------------------------------------- |
| Named Entity Recognition | `dslim/bert-base-NER`                                          |
| Summarization            | `facebook/bart-large-cnn`                                      |
| Semantic Similarity      | `sentence-transformers/all-MiniLM-L6-v2`                       |
| Cover Letter Generation  | `tiiuae/falcon-7b-instruct` or `mistralai/Mistral-7B-Instruct` |
| Interview Questions      | Prompted generation using above models                         |

---

## 🧱 System Architecture

**Microservice-Based Spring Boot App** with:

* JobParserService: Fetches and parses jobs from public APIs
* ResumeParserService: Parses user resumes
* MatcherService: Compares resume & job description embeddings
* GeneratorService: Uses LLMs for cover letters and interview questions
* REST API Gateway: Unified entrypoint

**Frontend Angular SPA** communicates via REST with full JWT auth.

---

## 📸 Screenshots

(TODO: Add screenshots showing resume matching, cover letter generation, etc.)

---

## 🚀 Getting Started

```bash
git clone https://github.com/MarcosLM11/JobGenieAI.git
cd JobGenieAI
# Start backend & frontend containers
docker-compose up --build
```

---

## 📅 Roadmap

* [ ] JobParserService
* [ ] ResumeParserService
* [ ] MatcherService
* [ ] GeneratorService
* [ ] Rest API Gateway
* [ ] Security
* [ ] Job listing filters by tech stack
* [ ] Job listing filters by tech stack
* [ ] Editable AI cover letter drafts
* [ ] Browser extension for LinkedIn jobs
* [ ] PDF export for application kits

---

## 👨‍💻 Author

\[Marcos López Marín] - Software Engineer passionate about AI, NLP, and career tech.

---

## 📜 License

MIT License

