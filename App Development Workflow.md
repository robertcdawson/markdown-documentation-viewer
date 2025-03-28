## App Development Workflow

### Step 1: Brainstorm MVP Features with Cursor
- **Tool Used**: Cursor (powered by Claude).
- [ ] **Action**: Work with Cursor to brainstorm and define the Minimum Viable Product (MVP) features.
- **Documents to Generate**:
  - **MVP Definition**: Core problem statement, target users, and essential features.
  - **Feature Prioritization**: Must-have vs. nice-to-have features.
  - **Success Metrics**: Key performance indicators and success criteria.
- **How**: Use clear prompts like:
  - "Help me define the MVP for [app name] focusing on core user needs."
  - "What are the essential features needed for the first version?"
- **Tip**: Keep the scope focused and avoid feature creep.

### Step 2: Review and Iterate on MVP with Cursor
- [ ] **Action**: Review and refine the MVP definition with Cursor.
- **How**: Use follow-up prompts like:
  - "Is this MVP scope too broad or too narrow?"
  - "What features could be moved to future iterations?"
- **Optional**: Share with stakeholders for early feedback.
- **Benefit**: Ensures a solid foundation before detailed documentation begins.

### Step 3: Generate Initial Documentation in Cursor
- **Tool Used**: Cursor (powered by Claude).
- [ ] **Action**: Instruct Cursor to create comprehensive initial documentation for your app idea in Markdown format.
- **Documents to Generate**:
  - **App Description (PRD)**: Overview, user flows, core features, in-scope vs. out-of-scope items, and target audience.
  - **Tech Stack with Guidelines**: Technologies, packages, dependencies, APIs, and usage instructions.
  - **UI/UX Instructions**: Fonts, color palette, spacing/layout rules, UI library, icon set, and accessibility guidelines.
  - **App Flow Doc**: Page-by-page navigation and user interactions in simple, non-bulleted text.
  - **Backend Structure Doc**: Database schema, authentication logic, storage rules, and edge cases.
  - **Implementation Plan**: 50+ specific, dependency-aware steps for coding the app.
- **How**: Use clear prompts specifying Markdown output. Examples:
  - "Generate an App Description (PRD) in Markdown format with sections for app overview, user flows, and core features."
  - "Create a Tech Stack document in Markdown listing Next.js, Supabase, and Tailwind CSS with usage guidelines."
- **Tip**: Include "in Markdown format" in every prompt and specify formatting (e.g., headers, lists, tables).

### Step 4: Review and Iterate on Documentation in Cursor

- [ ] **Action**: Review the generated Markdown documentation for clarity and completeness, then refine it with Cursor.
- **How**: Use follow-up prompts like:
  - "Revise the App Flow Doc to add a checkout page description in Markdown."
  - "Add a Markdown table to the Backend Structure Doc detailing the `users` table schema."
- **Optional**: Share with team members or experts for additional feedback.

### Step 5: Set Up Cursor with Documentation as Rules
- [ ] **Action**: Add all Markdown documentation as rules in Cursor to provide project context.
- **How**:
  1. Open Cursor's "Features" or "Project Knowledge" section.
  2. Upload each Markdown file or paste its contents into the rules area.
  3. Save to ensure Cursor uses this context for future tasks.
- **Benefit**: This gives the AI a detailed understanding of the project, reducing misinterpretations.

### Step 6: Instruct Cursor to Explain the App
- [ ] **Action**: Ask Cursor to summarize the app based on the documentation to verify its understanding.
- **Prompt Example**: "Based on the provided documentation, explain the app's purpose, key features, and tech stack in a few sentences."
- **Purpose**: Confirms the AI aligns with your vision before development begins.

### Step 7: Instruct Cursor to Create a TODO Document in Markdown
- [ ] **Action**: Have Cursor generate a TODO list in Markdown, breaking the project into actionable tasks based on the documentation.
- **Prompt Example**: "Using the documentation, create a TODO list in Markdown for building this app. Include frontend, backend, testing, and deployment tasks, marked as incomplete (e.g., `- [ ] Task`)."
- **Example Output** (for a fitness app):
  ```markdown
  # TODO List for Fitness App

  ## Frontend Tasks
  - [ ] Initialize Next.js with `npx create-next-app`.
  - [ ] Install Tailwind CSS for styling.
  - [ ] Build homepage with primary color #FF5733.

  ## Backend Tasks
  - [ ] Install Supabase client with `npm install @supabase/supabase-js`.
  - [ ] Create `users` table in Supabase with id and email fields.

  ## Testing Tasks
  - [ ] Write unit tests for authentication.

  ## Deployment Tasks
  - [ ] Deploy on Vercel with `vercel deploy`.
  ```
- **Rationale**: A granular TODO list keeps development focused and actionable.

### Step 8: Add the TODO Document as Project Knowledge in Cursor
- [ ] **Action**: Incorporate the TODO list into Cursor's knowledge base.
- **How**:
  1. In Cursor's "Project Knowledge" section, upload the TODO Markdown file or paste its contents.
  2. Save to ensure Cursor references it during development.
- **Benefit**: Enhances task prioritization and context awareness.

### Step 9: Instruct Cursor to Build the App with Task Dependencies
- [ ] **Action**: Guide Cursor to build the app step-by-step using the Implementation Plan and TODO list.
- **Prompt Example**: "Complete the next task from the TODO list: Initialize Next.js with `npx create-next-app`. Provide the setup code."
- **Tip**: Reference specific tasks and dependencies (e.g., "Set up Supabase authentication after creating the `users` table").
- **Optional**: Update the TODO list manually (e.g., `- [x] Task`) or ask Cursor to do it as tasks are completed.

### Step 10: Initialize Git, Create GitHub Repo, and Push
- [ ] **Action**: Set up version control by initializing a Git repository, creating a GitHub repo, and pushing the code and documentation (including the TODO list).
- **How**:
  - Run `git init`, `git add .`, `git commit -m "Initial commit"`.
  - Create a GitHub repo and push with `git push origin main`.
- **Optional**: Use GitHub issues for team task tracking.

### Step 11: Iterate, Push, and Repeat with Quality Assurance
- [ ] **Action**: Develop iteratively, using the TODO list as a guide, and apply quality assurance tools to maintain code quality.
- **Tools**:
  - **Linting**: ESLint for code consistency.
  - **Testing**: Unit tests (e.g., Jest) and end-to-end tests (e.g., Cypress).
- **How**: Run tests and linting regularly, then push updates to GitHub.
- **Tip**: Track progress by updating the TODO list or GitHub issues.

### Step 12: Host the App on Vercel (or Alternatives)
- [ ] **Action**: Deploy the app once it's stable, using Vercel or another platform based on project needs.
- **How**: Run `vercel deploy` for Vercel, or follow deployment steps for alternatives like Netlify or AWS.

### Step 13: Monitor, Refine, and Incorporate User Feedback
- [ ] **Action**: Monitor the app for issues and refine it based on user feedback.
- **Tools**: Google Analytics for usage tracking, Sentry for error monitoring.
- **How**: Conduct beta testing, gather feedback, and iterate as needed.
