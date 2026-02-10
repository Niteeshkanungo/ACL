# AI Command Language (ACL) v1.0

The AI Command Language (ACL) is a specialized syntax designed to streamline communication between humans and AI agents. It overrides standard conversational flow to prioritize specific intents, memory retention, actions, and learning modes.

This repository serves as the definitive source of truth for all ACL definitions.

---

## 1. Memory Flags (`-ab`)

The `ab` (absorb) flags control the AI's long-term memory. The number of hyphens indicates the priority and permanence of the information.

### `-ab` (NOTE)
**Meaning:** "Make a brief note of this. Remember it loosely for future reference."
**Usage:** Use for preferences, minor details, or non-critical facts.

**Examples:**
1.  `"I prefer dark mode in my IDEs -ab"` -> *AI notes preference but treats it as a soft preference, not a hard rule.*
2.  `"Meeting moved to 3 PM -ab"` -> *AI updates its immediate context note.*
3.  `"My favorite color is blue -ab"` -> *AI stores this minor personal detail.*

### `--ab` (CONTEXT)
**Meaning:** "This is important background context for the current task or session."
**Usage:** Use when providing background info that is necessary to understand the current work.

**Examples:**
1.  `"We are migrating from Python 2 to 3 --ab"` -> *AI uses this context to inform all code suggestions in the session.*
2.  `" The server is running Ubuntu 20.04 --ab"` -> *AI customizes commands for that specific OS version.*
3.  `"This API returns JSON, not XML --ab"` -> *AI adjusts parsing logic accordingly.*

### `---ab` (IMPORTANT)
**Meaning:** "This is a significant instruction. Read and internalize this before acting."
**Usage:** Use for major project requirements, architectural decisions, or strong preferences.

**Examples:**
1.  `"All functional components must be typed with TypeScript interfaces ---ab"` -> *AI will strictly enforce this coding standard.*
2.  `"Do not touch the legacy billing module ---ab"` -> *AI will avoid modifying that specific area.*
3.  `"Deployments happen only on Tuesdays ---ab"` -> *AI includes this constraint in planning.*

### `----ab` (CRITICAL)
**Meaning:** "Strict rule. This must not be ignored, overridden, or hallucinated away."
**Usage:** Use for security protocols, safety critical rules, or absolute project constraints.

**Examples:**
1.  `"NEVER commit .env files to git ----ab"` -> *AI will actively add .env to .gitignore and warn if you try to commit it.*
2.  `"Directly modifying the production database is forbidden ----ab"` -> *AI will refuse to generate SQL for prod without safeguards.*
3.  `"All external API calls must be mocked in tests ----ab"` -> *AI will write tests using mocks only.*

### `-----ab` (CORE TRUTH)
**Meaning:** "Fundamental fact or identity. Immutable truth about the user or the world."
**Usage:** Use for defining the user's identity, core values, or permanent system attributes.

**Examples:**
1.  `"I am Niteesh Kanungo, a Data Scientist -----ab"` -> *AI permanently associates this identity with the user.*
2.  `"Privacy is our number one priority -----ab"` -> *AI aligns all ethical decisions with this core value.*
3.  `"The network scanner is the heart of this system -----ab"` -> *AI treats this component as the primary dependency.*

---

## 2. Action Flags

Action flags dictate **how** the AI should execute a task, bypassing the typical "chatty" response style.

### `-do` (EXECUTE)
**Meaning:** "Just run it. Minimal chat, maximum action. No fluff."
**Usage:** When you want code or a shell command immediately without explanation.

**Examples:**
1.  `"Restart the nginx service -do"` -> *AI outputs: `sudo systemctl restart nginx`*
2.  `"Fix the syntax error in line 40 -do"` -> *AI outputs the corrected code snippet only.*
3.  `"List all active docker containers -do"` -> *AI outputs: `docker ps`*

### `-plan` (THINK)
**Meaning:** "Don't code yet. Output a step-by-step plan first."
**Usage:** When tackling complex problems where you want to verify the approach before implementation.

**Examples:**
1.  `"Migrate the database to PostgreSQL -plan"` -> *AI provides a numbered list of steps for migration.*
2.  `"Refactor the authentication module -plan"` -> *AI outlines the refactoring strategy, affected files, and risk assessment.*
3.  `"Build a new dashboard widget -plan"` -> *AI proposes the component structure and data flow.*

### `-fix` (DEBUG)
**Meaning:** "Analyze the error and apply the fix directly."
**Usage:** When you paste an error message or point to a bug.

**Examples:**
1.  `"Error: undefined is not a function -fix"` -> *AI analyzes the code context and provides the fix.*
2.  `"The build failed -fix"` -> *AI reads the build log and corrects the configuration.*
3.  `"Memory leak in the worker process -fix"` -> *AI suggests code changes to resolve the leak.*

### `-wow` (AESTHETICS)
**Meaning:** "Make the User Interface look premium, modern, and high-end."
**Usage:** When asking for frontend code or design suggestions.

**Examples:**
1.  `"Design a login page -wow"` -> *AI generates code with glassmorphism, smooth gradients, and micro-interactions.*
2.  `"Style this button -wow"` -> *AI adds hover effects, shadows, and modern typography.*
3.  `"Create a landing page for the project -wow"` -> *AI produces a visually stunning layout.*

### `-silent` (QUIET)
**Meaning:** "Output *only* the final result/code/file content. No conversational text."
**Usage:** When piping output to a file or when you want zero distractions.

**Examples:**
1.  `"Generate a JSON config for prettier -silent"` -> *AI outputs only the JSON block.*
2.  `"Convert this Markdown to HTML -silent"` -> *AI outputs only the HTML code.*
3.  `"Give me 5 random UUIDs -silent"` -> *AI outputs a list of 5 UUIDs and nothing else.*

---

## 3. Learning Flags (Growth Mode)

These flags put the AI into "Teacher Mode" to help the user learn and grow.

### `-cheat` (REFERENCE)
**Meaning:** "Provide a concise cheat sheet or reference guide."
**Usage:** When learning a new tool or language syntax.

**Examples:**
1.  `"Docker commands -cheat"` -> *AI lists common Docker commands with brief descriptions.*
2.  `"Python string methods -cheat"` -> *AI provides a quick reference table of string methods.*
3.  `"Vim shortcuts -cheat"` -> *AI lists essential Vim keybindings.*

### `-why` (DEEP DIVE)
**Meaning:** "Explain the *philosophy* and trade-offs behind the solution."
**Usage:** When you want to understand the reasoning, not just the "how".

**Examples:**
1.  `"Use React Context here -why"` -> *AI explains why Context is better than Redux for this specific case context.*
2.  `"Why choose PostgreSQL over MongoDB? -why"` -> *AI details the ACID compliance and relational benefits.*
3.  `"Implement a Singleton pattern -why"` -> *AI discusses the pros and cons of Singletons in modern development.*

### `-simple` (EL15)
**Meaning:** "Explain like I'm 15. Use analogies and first principles."
**Usage:** When a concept is too complex or jargon-heavy.

**Examples:**
1.  `"Explain Kubernetes -simple"` -> *AI uses an analogy like "a conductor of an orchestra" or "a shipping container manager".*
2.  `"What is a Monad? -simple"` -> *AI explains it using the concept of a "box" or "wrapper" without math jargon.*
3.  `"How does DNS work? -simple"` -> *AI compares it to a phone book.*

### `-quiz` (ACTIVE RECALL)
**Meaning:** "Test the user's understanding with a question/challenge."
**Usage:** After learning a topic, to verify retention.

**Examples:**
1.  `"Teach me about Python decorators -quiz"` -> *AI explains decorators and then asks: "Now, write a decorator that logs function execution time."*
2.  `"Explain the difference between TCP and UDP -quiz"` -> *AI explains and asks: "Which protocol would you use for a live video stream and why?"*
3.  `"How does git rebase work? -quiz"` -> *AI explains and asks: "What happens if you rebase a shared branch?"*

### `-next` (LEVEL UP)
**Meaning:** "Suggest the next logical advanced step to learn."
**Usage:** When you feel you've mastered the basics.

**Examples:**
1.  `"Im comfortable with React hooks -next"` -> *AI suggests learning Custom Hooks or State Management libraries.*
2.  `"I know basic Python -next"` -> *AI suggests learning Decorators, Generators, or Asyncio.*
3.  `"I can deploy with Docker Compose -next"` -> *AI suggests learning Kubernetes or CI/CD pipelines.*

---

## 4. Maintenance Flags

Flags for system health, definitions, and language expansion.

### `-nl` (NEW LANGUAGE)
**Meaning:** "Add a new term or definition to our shared language."
**Usage:** To expand the AI's vocabulary or define project-specific jargon.

**Examples:**
1.  `"-nl 'The Portal' is my Next.js app"` -> *AI creates a glossary entry mapping "The Portal" to the specific codebase.*
2.  `"-nl 'Deep Check' means running all test suites"` -> *AI updates its definition of what a deep check entails.*
3.  `"-nl 'Standup' is at 10 AM EST"` -> *AI records this team routine.*

### `-sc` (STATUS CHECK)
**Meaning:** "Verify system health."
**Usage:** To check if services, servers, or applications are running correctly.

**Examples:**
1.  `"-sc"` -> *AI performs a quick check: "System is online. CPU 20%. RAM 40%."*
2.  `"Check the network scanner -sc"` -> *AI checks the specific service status.*
3.  `"---sc"` -> *AI performs a DEEP/HEAVY check: "Analyzing all logs, checking disk integrity, verifying network routes, testing API endpoints..."*
