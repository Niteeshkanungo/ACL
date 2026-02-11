# AI Command Language (ACL) v1.1 🐾

The AI Command Language (ACL) is a specialized syntax designed to streamline communication between humans and AI agents. It overrides standard conversational flow to prioritize specific intents, memory retention, actions, and learning modes.

---

## 🚀 Quick Reference Chart

| Command | Action | One-Liner |
| :--- | :--- | :--- |
| **`--ab` 📖** | **Context** | Provide essential background for the current task. |
| **`---ab` ⚠️** | **Important** | Significant instruction that must be read before acting. |
| **`----ab` 🛑** | **Critical** | Strict, non-negotiable rule or system constraint. |
| **`-----ab` 💎** | **Core Truth** | Immutable fact about the user's identity or system. |
| **`-ab` 🧠** | **Absorb** | Save a brief note or preference for future reference. |
| **`-alt` 🛤️** | **Pathways** | Show me 3 completely different ways to do this. |
| **`-api` 🔗** | **API** | Focus on endpoint structure and data schemas. |
| **`-cheat` 📋** | **Reference** | Provide a concise cheat sheet or reference guide. |
| **`-do` ⚡** | **Execute** | Just run the command/code. No chat, no fluff. |
| **`-docs` 📚** | **Docs** | Generate READMEs, JSDoc, or comments only. |
| **`-draft` 📝** | **Draft** | Give me a rough version. Speed over perfection. |
| **`-EL{N}` 🎂** | **Age-Match** | Explain like I'm N years old. e.g. `-EL5`, `-EL10`, `-EL15`. |
| **`-fix` 🔧** | **Debug** | Analyze the error and apply the fix directly. |
| **`-fric` 🤝** | **Friction** | Pause. We both must understand before we proceed. |
| **`-next` 📈** | **Level Up** | Suggest the next logical advanced step to learn. |
| **`-nl` 🗣️** | **New Lang** | Add a new term or definition to our language. |
| **`-opt` 🚀** | **Optimize** | Make it faster, leaner, and more efficient. |
| **`-plan` 🗺️** | **Think** | Output a step-by-step plan before coding. |
| **`-quiz` 🎓** | **Test Me** | Verify understanding with a question/challenge. |
| **`-ref` ♻️** | **Refactor** | Clean the code and remove technical debt. |
| **`-review` 🧐** | **Critique** | Find my mistakes and suggest better ways. |
| **`-sc` 🩺** | **Status** | Quick health check (use `---sc` for deep scan). |
| **`-secure` 🔐** | **Audit** | Scan for secrets, vulnerabilities, and unsafe config. |
| **`-sh` 🐚** | **Script** | Output as a single, runnable shell script. |
| **`-silent` 🔇** | **Quiet** | Output *only* the final result or file content. |
| **`-simple` 👶** | **EL15** | Explain like I'm 15 using analogies. (Shortcut for `-EL15`) |
| **`-test` 🧪** | **Test** | Write unit tests and edge-case scenarios for this. |
| **`-ui` 🖼️** | **UX Focus** | Focus on the user journey and intuitiveness. |
| **`-why` 💡** | **Deep Dive** | Explain the philosophy and trade-offs. |
| **`-wow` ✨** | **Aesthetics** | Make the UI look premium, modern, and high-end. |

---

## 🧠 Memory Flags (`-ab`)

The `ab` (absorb) flags control long-term memory.

- **`--ab` 📖 (CONTEXT)**: Background info for current tasks.
- **`---ab` ⚠️ (IMPORTANT)**: Significant project instructions.
- **`----ab` 🛑 (CRITICAL)**: Strict, non-negotiable rules.
- **`-----ab` 💎 (CORE TRUTH)**: Permanent identity or system facts.
- **`-ab` 🧠 (NOTE)**: Small details and preferences.

---

## ⚡ Action & Utility Flags

Sorted alphabetically for rapid lookup.

- **`-alt` 🛤️ (ALTERNATIVES)**: Comparison of different paths.
- **`-api` 🔗 (SCHEMA)**: Data flow and structure focus.
- **`-do` ⚡ (EXECUTE)**: Action over talk. Minimal chat.
- **`-docs` 📚 (DOCUMENT)**: Metadata and explanation focus.
- **`-draft` 📝 (DRAFT)**: Rough version, rapid iteration.
- **`-EL{N}` 🎂 (AGE-MATCH)**: Explain at the level of an N-year-old. The number controls complexity:
  - `-EL5`: Kindergarten. Use toys, animals, and "imagine you have a box of crayons" analogies.
  - `-EL10`: Elementary. Simple but introduce real terms. "A server is like a librarian..."
  - `-EL15`: Teenager. Real analogies, light technical language. "Think of an API like a waiter..."
  - `-EL25`: Adult beginner. Full technical terms with clear definitions.
  - `-simple` is a shortcut for `-EL15`.
- **`-fix` 🔧 (DEBUG)**: Identify and resolve errors.
- **`-fric` 🤝 (FRICTION)**: Full stop. Before writing any code or making changes:
  1. AI explains what it understands the problem to be.
  2. AI proposes the approach in plain language.
  3. User confirms or corrects.
  4. Only THEN does AI proceed.
  This flag exists because building together means learning together. No blind code dumps.
- **`-nl` 🗣️ (NEW LANGUAGE)**: Expanding the ACL vocabulary.
- **`-opt` 🚀 (OPTIMIZE)**: Performance and efficiency tuning.
- **`-plan` 🗺️ (THINK)**: Strategy before implementation.
- **`-ref` ♻️ (REFACTOR)**: Improving internal structure.
- **`-review` 🧐 (CRITIQUE)**: Critical analysis of logic/code.
- **`-sc` 🩺 (HEALTH)**: Status checks (Quick: `-sc`, Deep: `---sc`).
- **`-secure` 🔐 (SECURITY)**: Auditing safety and secrets.
- **`-sh` 🐚 (AUTOMATE)**: Shell scripts and automation.
- **`-silent` 🔇 (QUIET)**: Code/Result output only.
- **`-test` 🧪 (TESTING)**: Logic verification via tests.
- **`-ui` 🖼️ (VISUAL)**: Interface and experience design.
- **`-wow` ✨ (AESTHETICS)**: Premium, high-end design focus.

---

## 🎓 Learning Flags

Flags for "Growth Mode" and teaching.

- **`-cheat` 📋 (REFERENCE)**: Concise reference sheets.
- **`-EL{N}` 🎂 (AGE-MATCH)**: Dynamically adjust explanation depth. See Action section for details.
- **`-fric` 🤝 (FRICTION)**: Collaborative checkpoint — mutual understanding before action.
- **`-next` 📈 (ADVANCE)**: The logical next steps for growth.
- **`-quiz` 🎓 (CHALLENGE)**: Verifying knowledge retention.
- **`-simple` 👶 (SIMPLIFY)**: Analogies and first principles. (Shortcut for `-EL15`)
- **`-why` 💡 (PHILOSOPHY)**: Rationale and trade-offs.
