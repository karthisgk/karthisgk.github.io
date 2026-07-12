---
name: tailor_resume
description: Tailors the user's resumes (new.html and v2.html) based on a job description (JD) or target position.
---

# Tailor Resume Skill

This skill automates the process of tailoring the user's detailed (2-page) and condensed (1-page) resumes to match a specific job description (JD) or target role (e.g., MERN stack position, AI integration developer, company-specific profiles like Infosys).

## When to use this skill
Use this skill when:
* The user requests to rewrite, tailor, adapt, or update their resumes (`new.html` and/or `v2.html`) for a specific target position, job posting, or company profile.
* You need to customize the resume content to highlight specific technologies (e.g., MERN stack, NodeJS), methodologies, or job responsibilities.
* You need to create tailored variants of the resumes while keeping their original visual layouts and styles completely intact.

## Execution Guidelines

### 1. Retrieve the Job Description (JD) Source
* If the user has not provided the job description or target position:
  * **Ask the user to provide the JD source.** The source can be a raw text description, a website copy-paste, or details about the role/company.
  * Wait for the user's response containing the JD details.

### 2. Read the Resume Templates
* Read the base resume template files:
  * Detailed 2-page template: [resume/new.html](file:///Users/karthicksg/Documents/karthisgk_git/karthisgk.github.io/resume/new.html)
  * Condensed 1-page template: [resume/v2.html](file:///Users/karthicksg/Documents/karthisgk_git/karthisgk.github.io/resume/v2.html)

### 3. Analyze the Job Description (JD)
Extract critical requirements from the JD:
* **Target Job Title & Company Name**: (e.g. "Senior Full-Stack Developer" at "Infosys").
* **Core Technologies**: Highlight key technologies mentioned (e.g., MERN stack, MongoDB, Express, React, Node.js, JWT, Git, AI APIs, etc.).
* **Key Responsibilities**: Map experience bullets to highlight frontend UX/reusable components, secure API design, database schema optimization, testing/code reviews, and AI-enabled feature delivery.
* **Education & Experience**: Highlight matching years of experience (e.g. 5+ years) and relevant degrees (e.g., MCA, B.Sc IT).

### 4. Create the Tailored Resumes (Content-Only)
Tailor the text content of both resumes to align with the extracted JD requirements. 

> [!IMPORTANT]
> **CRITICAL RULE**: Do NOT modify, delete, or add any CSS styles, styling attributes, layout classes (e.g. `.page`, `.skills-grid`, `.job`), font definitions, or grid setups. You are strictly modifying the text inside the HTML tags to preserve the exact UI.

#### Tailoring Specifications:
* **Title & Header**: Set the header title to reflect the target role.
* **Summary Box**: Focus on matching experience (e.g. MERN stack, Node.js, React, secure REST APIs, MongoDB, LLM integration, and data privacy) in a clean paragraph.
* **Core Skills Grid**: Align grid elements to highlight the JD's requested skills. Keep the exact number of grid cells:
  * Exactly **14** skill items in the 2-page detailed resume.
  * Exactly **12** skill items in the 1-page condensed resume.
* **Professional Experience Bullets**:
  * Emphasize keywords and tasks from the JD (MERN stack development, query optimization, secure APIs, JWT authentication, code reviews, writing testable code, CI/CD, product/design/QA collaboration, and technical documentation).
* **Notable Projects**: Highlight how your projects (MCP Expense Tracker, Telegram AI chatbot, multi-tenant healthcare/finance backends, open-source packages) match the JD requirements.

### 5. Write the Files to Target Directories
Save the tailored resumes under a company or role-specific subdirectory:
* Determine a folder name from the company or role (e.g., `resume/infosus/` or `resume/<normalized_role_name>/`).
* Write the detailed version to `<target_dir>/two-page/index.html`.
* Write the condensed version to `<target_dir>/one-page/index.html`.

### 6. Verify and Document
* Validate that both files are properly formatted HTML documents and do not contain syntax errors or stray characters.
* Verify that the print previews render correctly (especially that the 1-page version fits cleanly onto exactly one page).
* Provide the user with links to the generated files and a walkthrough detailing the content optimizations.
