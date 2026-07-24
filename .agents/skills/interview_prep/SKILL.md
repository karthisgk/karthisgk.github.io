---
name: generate_interview_prep
description: Generates a comprehensive interview preparation plan and interactive study material web UI based on a job description (JD) or target position.
---

# Generate Interview Prep Skill

This skill creates a complete, interactive, course-style interview preparation portal and study guide tailored to a specific Job Description (JD) or target position (e.g., Senior MERN Developer at Infosys, GCP Big Data Engineer at Amex, Full-Stack Engineer at Google).

The generated output is an interactive, standalone single-page web application (LMS/online-course dashboard style) stored in a company or role-specific directory (e.g., `interview_prep/<company_or_role>/index.html`).

---

## When to use this skill
Use this skill when:
* The user asks for an interview preparation plan, study guide, or question bank based on a job description or company target.
* The user wants structured technical study materials, system design breakdowns, coding prep, or behavioral Q&A formatted as an interactive web app or course platform.
* The user provides a JD (or company/role name) and requests interview prep resources.

---

## Execution Guidelines

### 1. Retrieve the Job Description (JD) Source
* If the user has not provided a JD or target position:
  * **Prompt the user** to provide the JD text, target role title, or target company name.
  * Wait for the user's input before generating the prep plan.

### 2. Analyze the Job Description (JD)
Extract and categorize all key requirements:
* **Target Company & Role**: (e.g. American Express — Senior Big Data Engineer, Infosys — MERN Stack Developer).
* **Core Technical Domains**: (e.g., Node.js, React, MongoDB, GCP BigQuery, Spark, Kafka, Spring Boot, System Design).
* **Required Experience & Seniority Level**: (e.g. Senior / Lead level vs. Mid level, focus on architecture & team leadership vs. hands-on syntax).
* **Key Non-Technical / Behavioral Areas**: (e.g., Agile/SAFe, cross-functional collaboration, security & risk mindset, team mentoring).
* **AI & Modern Capabilities**: (e.g., GenAI integration, LLMs, prompt engineering, low-code/no-code workflows).

### 3. Design & Develop the Course Web UI (`index.html`)
The output must be a self-contained, fully interactive, premium online-course dashboard (styled like Educative, Coursera, or Udemy) saved at `interview_prep/<normalized_company_or_role>/index.html`.

#### UI/UX & Design System Requirements (Standard LMS Dashboard Pattern):
* **Design System**: Slate/Navy CSS custom properties (`--bg-primary`, `--bg-secondary`, `--accent-cyan`, `--border-color`) with full dark/light theme toggle.
* **Typography**: Google Fonts `Inter` + `JetBrains Mono` for code blocks.
* **Layout**: Left-hand collapsible sidebar navigation (`310px`) with search filter, course modules list, and progress reset; sticky top bar showing overall completion progress (% complete, study time estimate, streak indicator); hero banner with role tags and stat cards.
* **Interactive Component Suite (Vanilla JS inside HTML)**:
  * Module/Lesson navigation tab switching without page reload.
  * Interactive checkboxes for marking lessons/topics complete (persisting progress in `localStorage`).
  * 3D Flip Flashcards for rapid concept revision.
  * Collapsible/expandable accordions for interview questions and model answers with difficulty badges (`Easy`, `Medium`, `Hard`, `Must-Know`).
  * Code blocks with header bar and 1-click clipboard copy functionality.
  * Practice quiz widget with immediate visual correct/incorrect feedback.
  * Real-time search input filtering module contents.

---

## Content Blueprint for Generated Study Material

The generated prep portal MUST contain rich, detailed, role-specific content divided into structured modules:

### Module 1: Overview & JD Breakdown
* Target Role Breakdown & Key Competencies evaluated by interviewer.
* Company Background & Engineering Culture notes (e.g., Amex risk & reliability mindset, Infosys digital transformation).
* 7-Day / 14-Day Study Plan Roadmap timeline.

### Module 2: Core Technical Deep Dives (Role-Specific)
* Comprehensive study notes and cheat sheets on each core tech required by the JD.
* Deep-dive concepts, internal workings, edge cases, and performance tuning rules (e.g., BigQuery indexing/partitioning, MongoDB indexing, React rendering lifecycle, Node.js event loop, Kafka partitioning, Spring Boot bean lifecycle).

### Module 3: Coding & Problem Solving
* Top coding patterns and algorithms relevant to the role.
* Hand-picked interview questions with problem statements, key takeaways, time/space complexity analysis, and syntax code blocks.

### Module 4: System Design & Architecture
* Architecture blueprints & design problems tailored to the JD (e.g., "Design a Real-Time Big Data Ingestion Pipeline for Financial Transactions" or "Design a Scalable Multi-Tenant MERN Platform").
* Component breakdown, data flows, scalability/trade-off decisions, high availability, and DR setup strategies.

### Module 5: Behavioral & Leadership (STAR Method)
* Behavioral questions aligned with company core values and leadership principles.
* Structured **STAR** (Situation, Task, Action, Result) model response templates pre-filled with context from the user's background.

### Module 6: Mock Interview Question Bank
* Categorized question bank (Technical, System Design, Scenario/Troubleshooting).
* Toggleable "Show Answer / Explanation" accordions for self-testing.

---

## 4. Verification & Output Deliverables
1. Write the completed standalone web application to `interview_prep/<normalized_name>/index.html`.
2. Open/verify the HTML output to ensure all scripts, styles, and interactive tabs work smoothly.
3. Present a clear summary to the user with a clickable link to the generated prep portal file (`interview_prep/.../index.html`).
