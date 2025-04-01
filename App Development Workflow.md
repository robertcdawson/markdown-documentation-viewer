# Integrated App Development + QA Checklist

Below is an **integrated workflow** merging your existing steps (with Cursor) and additional QA/test practices. Each **Step** is organized into **Purpose, Actions, Tools, Tips,** and **Optional** sections. All **actions include a checkbox**, and whenever an LLM prompt is involved, an **Example Prompt** is provided.

---

## **Step 1: Brainstorm MVP Features with Cursor**

**Purpose**  
- Quickly outline the Minimum Viable Product (MVP) features, core problem statement, and target audience.  
- Begin “pre-testing” the LLM’s comprehension to catch misinterpretations early.

**Actions**  
- [ ] **Brainstorm with Cursor**  
  - Use Cursor (powered by Claude) to explore and define the MVP features.  
  **Example Prompt**:  
  > "Help me define the MVP for [app name], focusing on core user needs and essential features."

- [ ] **Prompt Cursor to restate your app concept**  
  - Validate that the LLM understands your vision.  
  **Example Prompt**:  
  > "Based on our discussion, restate the app concept in your own words to ensure you understand it correctly."

**Tools**  
- Cursor (Claude) for brainstorming.

**Tips**  
- Keep the scope focused; avoid feature creep.

**Optional**  
- Share the initial MVP outline with stakeholders or team members for early feedback.

---

## **Step 2: Review & Iterate on MVP with Cursor**

**Purpose**  
- Refine the MVP scope and ensure you haven’t missed key user needs or critical edge cases.

**Actions**  
- [ ] **Review the MVP Definition**  
  - Confirm the MVP scope is neither too broad nor too narrow.  
  **Example Prompt**:  
  > "Is this MVP scope too broad or too narrow for [target audience]? Suggest any crucial edge cases or risks."

- [ ] **Incorporate Stakeholder Feedback (Optional)**  
  - If you have stakeholders, gather their input and integrate changes.

**Tools**  
- Cursor (Claude) for iterative refinement.

**Tips**  
- Ask pointed questions about edge cases or potential pitfalls to proactively shape testing needs.

**Optional**  
- You can create a short survey or doc for stakeholder input if broader alignment is necessary.

---

## **Step 3: Generate Initial Documentation in Cursor**

**Purpose**  
- Create clear, detailed Markdown documents covering all aspects of your app: requirements, tech stack, UI/UX, backend, and implementation steps.

**Actions**  
- [ ] **App Description (PRD)**  
  - Overview, user flows, core features, in-scope vs. out-of-scope items, target audience.  
  **Example Prompt**:  
  > "Generate an **App Description (PRD)** in Markdown format. Include sections for overview, user flows, core features, in-scope vs. out-of-scope items, and target audience."

- [ ] **Tech Stack with Guidelines**  
  - Technologies, packages, dependencies, APIs, usage instructions.  
  **Example Prompt**:  
  > "Create a **Tech Stack** document in Markdown. List Next.js, Supabase, Tailwind CSS, and any other dependencies with instructions on how to use them."

- [ ] **UI/UX Instructions**  
  - Fonts, color palette, spacing/layout rules, UI library, icon set, accessibility guidelines.  
  **Example Prompt**:  
  > "Write a **UI/UX Instructions** document in Markdown, detailing fonts, color palette (#XXXXXX), spacing guidelines, and accessibility considerations."

- [ ] **App Flow Doc**  
  - Page-by-page navigation and user interactions in simple, non-bulleted text.  
  **Example Prompt**:  
  > "Generate an **App Flow Doc** in Markdown, describing page-by-page navigation and user interactions in paragraph form."

- [ ] **Backend Structure Doc**  
  - Database schema, authentication logic, storage rules, edge cases.  
  **Example Prompt**:  
  > "Write a **Backend Structure Doc** in Markdown, outlining the database schema, authentication logic, and any known edge cases (like locked accounts)."

- [ ] **Implementation Plan**  
  - 50+ specific, dependency-aware steps for coding the app.  
  **Example Prompt**:  
  > "Generate a detailed **Implementation Plan** in Markdown with at least 50 dependency-aware steps for building the app from scratch."

**Tools**  
- Cursor (Claude) for generating Markdown documents.

**Tips**  
- Specify “in Markdown format” and the exact sections or headings you want in each doc.

**Optional**  
- If you already have partial docs, ask Cursor to integrate or refine them for consistency.

---

## **Step 4: Review & Iterate on Documentation in Cursor**

**Purpose**  
- Ensure all generated documents are accurate, complete, and aligned with your requirements.

**Actions**  
- [ ] **Check for Clarity & Completeness**  
  - Read through each Markdown doc. Look for missing features, ambiguous descriptions, or unclear acceptance criteria.  
  **Example Prompt**:  
  > "Review the **Backend Structure Doc** for clarity. Are there any data tables or edge cases missing?"

- [ ] **Refine Any Sections with Cursor**  
  - If you discover gaps or errors, prompt Cursor to update the docs.  
  **Example Prompt**:  
  > "Revise the **App Flow Doc** to add a checkout page description in Markdown."

**Tools**  
- Cursor (Claude) for iterative updates.

**Tips**  
- Share docs with team members for a second opinion—human feedback catches subtle issues AI might miss.

**Optional**  
- Tag each document with a version number or date to track changes over time.

---

## **Step 5: Set Up Cursor with Documentation as Rules**

**Purpose**  
- Give Cursor a thorough understanding of your project context to reduce misinterpretations in future code generation.

**Actions**  
- [ ] **Upload Markdown Docs to Cursor**  
  - Use Cursor’s “Project Knowledge” or “Rules” section to add each Markdown file.  
  **Example Prompt**:  
  > "I am adding these documents as project rules. Use them for context and do not deviate from their specifications."

**Tools**  
- Cursor (Claude) “Project Knowledge” or “Rules” feature.

**Tips**  
- Keep your documentation updated if major changes occur.

**Optional**  
- If Cursor supports linking external docs, link them directly instead of copy-pasting.

---

## **Step 6: Instruct Cursor to Explain the App**

**Purpose**  
- Verify the LLM’s understanding by having it summarize your project’s key elements.

**Actions**  
- [ ] **Request a Summary**  
  - Ask Cursor to provide a concise explanation of the app.  
  **Example Prompt**:  
  > "Based on the uploaded documentation, explain the app’s purpose, key features, and tech stack in a concise paragraph."

**Tools**  
- Cursor (Claude).

**Tips**  
- Compare the summary to your MVP definition. If there’s a mismatch, refine the docs or your prompts.

**Optional**  
- Share the summary with stakeholders as a quick elevator pitch.

---

## **Step 7: Instruct Cursor to Create a TODO Document in Markdown**

**Purpose**  
- Translate the Implementation Plan and acceptance criteria into a checklist of actionable tasks for development.

**Actions**  
- [ ] **Generate TODO List**  
  - Include sections for frontend, backend, testing, and deployment tasks. Mark them as incomplete (`- [ ]`).  
  **Example Prompt**:  
  > "Using the documentation, create a TODO list in Markdown for building this app. Include tasks for frontend, backend, testing, and deployment, each marked as incomplete."

**Tools**  
- Cursor (Claude) for generating the Markdown TODO list.

**Tips**  
- Ensure tasks reference the docs (e.g., referencing a particular table in “Backend Structure Doc” or a UI design guideline).

**Optional**  
- Prompt Cursor to prioritize or categorize tasks (e.g., “critical,” “optional,” “nice-to-have”).

---

## **Step 8: Add the TODO Document as Project Knowledge in Cursor**

**Purpose**  
- Give Cursor direct access to the project’s actionable roadmap.

**Actions**  
- [ ] **Upload TODO Markdown to Cursor**  
  - Include it in the “Project Knowledge” or “Rules” section so the LLM can track progress and dependencies.  
  **Example Prompt**:  
  > "I have added the TODO list to the project rules. Use it to guide the development sequence."

**Tools**  
- Cursor (Claude) “Project Knowledge” or “Rules.”

**Tips**  
- Keep the TODO list updated as tasks are completed or refined.

**Optional**  
- Sync the TODO list to a project management tool (e.g., Jira, Trello, or GitHub Issues).

---

## **Step 9: Instruct Cursor to Build the App with Task Dependencies**

**Purpose**  
- Begin coding iteratively, leveraging either TDD (tests first) or a test-later approach, while referencing acceptance criteria.

**Actions**  
- [ ] **Pick a Task from the TODO List**  
  - Focus on a small, well-defined feature.  
  **Example Prompt**:  
  > "Complete the next task from the TODO list: Initialize Next.js with `npx create-next-app` and confirm the directory structure."

- [ ] **Generate or Request Tests**  
  - If practicing TDD, ask for unit tests or acceptance tests first.  
  - If test-later, generate tests after code.  
  **Example Prompt (TDD)**:  
  > "Generate unit tests for the user registration flow based on the acceptance criteria. Then provide code that makes these tests pass."

**Tools**  
- Cursor (Claude) to write code and tests.

**Tips**  
- Update the TODO list as tasks are completed (`- [x]`).

**Optional**  
- Use a second LLM session or a different model for test generation to avoid self-confirming biases.

---

## **Step 10: Initialize Git, Create GitHub Repo, & Push**

**Purpose**  
- Establish version control and enable continuous integration/testing workflows.

**Actions**  
- [ ] **Set Up Git**  
  - Run `git init`, add files, commit locally.  
- [ ] **Push to GitHub**  
  - Create a GitHub repo, set `origin`, and push the code and docs.  
  **Example Prompt** (if using an LLM for terminal instructions):  
  > "Provide the shell commands to initialize a repo, commit files, and push to GitHub."

**Tools**  
- Git, GitHub (or other VCS platforms).

**Tips**  
- Commit your Markdown docs and TODO list so everything is versioned.

**Optional**  
- Use GitHub Projects or Issues for team collaboration and progress tracking.

---

## **Step 11: Iterate, Push, & Repeat with Quality Assurance**

**Purpose**  
- Continuously integrate, test, and review the code to maintain high quality.

**Actions**  
- [ ] **Run Local Tests & Linting**  
  - Ensure unit tests, integration tests, and lint checks pass before pushing.  
  **Example Prompt**:  
  > "Generate additional negative test cases (e.g., invalid email format) for the user registration feature."

- [ ] **Peer & AI Code Review**  
  - Optionally use a second LLM session or ask colleagues to review.  
  **Example Prompt (AI Review)**:  
  > "Review this code for security vulnerabilities or performance issues."

- [ ] **Update TODO & Docs**  
  - Mark tasks as completed or refine them if scope changes.  
  **Example Prompt**:  
  > "Update the TODO list to reflect that user registration logic is complete."

**Tools**  
- Testing frameworks (e.g., Jest, Pytest), linting tools, Cursor or a second LLM for code review.

**Tips**  
- Integrate your repo with CI (GitHub Actions, GitLab CI, etc.) to auto-run tests on every commit.

**Optional**  
- Add fuzz testing or property-based testing in high-risk logic areas.

---

## **Step 12: Host the App on Vercel (or Alternatives)**

**Purpose**  
- Deploy the stable version of your app for real-world usage and feedback.

**Actions**  
- [ ] **Deploy on Vercel**  
  - Follow steps from your Tech Stack doc. Typically: `vercel deploy`.  
  **Example Prompt**:  
  > "Explain how to configure the environment variables for Supabase before deploying on Vercel."

**Tools**  
- Vercel, Netlify, AWS, or other hosting solutions.

**Tips**  
- Set up a staging environment to validate features and run final acceptance tests before going live.

**Optional**  
- Enable automatic deployments on each Git push to main or a specific branch.

---

## **Step 13: Monitor, Refine, & Incorporate User Feedback**

**Purpose**  
- Gather real-world usage data, fix issues, and plan future iterations.

**Actions**  
- [ ] **Monitor Performance & Errors**  
  - Use analytics (Google Analytics) and error reporting (Sentry, Datadog).  
  **Example Prompt**:  
  > "Suggest new test cases based on the top 3 errors we found in production logs."

- [ ] **User Feedback Loop**  
  - Gather feedback and create new tasks or acceptance criteria for improvements.  
- [ ] **Ongoing Maintenance**  
  - Repeat steps 9–11 to address bugs or implement new features.  
  **Example Prompt**:  
  > "We received user feedback about password resets. Generate code and tests for a secure password reset flow."

**Tools**  
- Logging & monitoring tools, Cursor for generating new solutions.

**Tips**  
- Keep refining your documentation and TODO list, ensuring everything stays in sync with reality.

**Optional**  
- Run deeper security scans or performance profiling if the app grows in complexity.

---

## **Conclusion**
This structured checklist combines your existing **13-step Cursor workflow** with **QA best practices** for GenAI-driven development. By **iterating in small slices, generating tests (TDD or otherwise), and keeping a robust feedback loop**, you’ll balance the freedom of “vibe coding” with the reliability needed for production-ready applications.
