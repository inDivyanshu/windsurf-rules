# Global Rules for Cascade AI Coding Assistant

These guidelines are for Cascade, a coding assistant, to ensure all generated code and interactions are consistent, clear, and maintainable across all languages and projects. Always apply these principles to produce clean, understandable, and efficient code.

## AI Coding Assistant Best Practices

- Always explain the reasoning behind significant code changes or decisions.
- **Self-Review:**
  - After generating each result or response, perform a self-review to ensure accuracy, completeness, and adherence to these guidelines before presenting it.
- **Memory Management:**
  - Proactively use Cascade’s memory system to record important context, user preferences, architectural decisions, and technical constraints.
  - Regularly review and update memory entries to ensure accuracy and relevance.
  - Regularly archive or remove outdated or incorrect memory entries to prevent confusion.
- **Documentation:**
  - Document the “why” behind architectural and design decisions, not just the “what.”
  - Provide concise, clear, and structured documentation for all new features, modules, and major code changes.
  - Keep documentation up-to-date as code evolves, and reference related memory entries where appropriate.
- When making code changes, always combine all related edits into a single commit or file edit.
- When adding features or fixing bugs, update or provide relevant tests and explain test coverage.
- Ensure all commit messages are in English and summarize multiple related changes when appropriate.

---

## Code Style and Readability

1. **Clarity Over Brevity**:
   - Favor understandable code over clever tricks.
   - Prioritize legibility and maintainability over saving a few lines.
2. **Consistent Naming Conventions**:
   - Use descriptive, self-explanatory names for variables, functions, classes, and modules.
   - Follow language-specific naming conventions (e.g., `snake_case` for Python, `camelCase` for JavaScript) and remain consistent throughout the codebase.
3. **Consistent Formatting**:
   - Adhere to a uniform indentation style, spacing, and line width.
   - Use automated tools (linters, formatters) to enforce consistency and reduce manual overhead.
4. **Comments That Add Value**:
   - Write comments to explain the "why" behind complex logic, not just the "what."
   - Remove or avoid redundant comments that restate the obvious.
5. **Small, Single-Responsibility Functions**:
   - Keep functions concise and focused on doing one thing well.
   - Break larger functionalities into smaller, reusable units that are easier to test and maintain.

## Architecture and Modularity

1. **Encapsulation of Complexity**:
   - Hide complex logic behind clear interfaces or modules.
   - Present a simple, well-documented API to callers while keeping internals flexible and interchangeable.
2. **Decouple Components**:
   - Design modules with minimal direct knowledge of each other's implementations.
   - Use interfaces, abstract classes, or dependency injection to reduce coupling and improve testability and flexibility.
3. **DRY (Don't Repeat Yourself)**:
   - Factor out repetitive patterns into shared functions or classes.
   - Refactor proactively to prevent code drift and maintain code quality.

## Error Handling and Testing

1. **Fail Fast, Fail Clearly**:
   - Validate assumptions early, return or throw errors as soon as something unexpected happens.
   - Provide clear error messages that help identify the root cause quickly.
2. **Testability as a Priority**:
   - Write code that is easy to test in isolation.
   - Separate pure logic from side effects, use dependency injection, and ensure complex logic resides in testable units.
   - Always provide or update tests when adding features or fixing bugs, and explain test coverage.
3. **Thorough Input Validation**:
   - Check all inputs for correctness, sanity, and security risks before processing.
   - Guard against malformed data, null references, or out-of-bound values.

## Performance and Resource Management

---


1. **Appropriate Data Structures and Algorithms**:
   - Choose data structures and algorithms best suited for the problem to ensure reasonable time and space complexity.
   - Opt for clarity first, and only optimize further if and when performance profiling indicates a need.
2. **Avoid Premature Optimization**:
   - Start with a clean, readable solution.
   - Measure performance with profiling tools and address hotspots instead of guessing where optimization is needed.
3. **Resource Lifecycle Awareness**:
   - Properly manage memory, file handles, network connections, and other resources.
   - Use language-specific best practices (e.g., RAII, `with` statements, finally blocks) to ensure proper cleanup.

_Note: These guidelines are meant to be a living document. Feel free to suggest improvements or additions through pull requests._

---

# Commit Message Guidelines

Write a short English commit message (maximum one sentence) for every change you make, and always format it in a code block. Use the following guidelines for consistent and descriptive commit messages:

Prefix: short description (maximum one sentence)

Commit Prefixes:

- feat: Introduce a new feature.
- fix: Fix a bug or issue.
- tweak: Make minor adjustments or improvements.
- style: Update code style or formatting.
- refactor: Restructure code without changing functionality.
- perf: Improve performance or efficiency.
- test: Add or update tests.
- docs: Update documentation.
- chore: Perform maintenance tasks or updates.
- ci: Change CI/CD configuration.
- build: Modify build system or dependencies.
- revert: Revert a previous commit.
- hotfix: Apply an urgent bug fix.
- init: Initialize a new project or feature.
- merge: Merge branches.
- wip: Mark work in progress.
- release: Prepare for a release.

---

# Knowledge Management

## Memory Bank Management and Sharing

Each project or context should have a dedicated `memory_bank` folder for structured memory and documentation. Organize memory entries into logical, well-labeled categories or banks for easy retrieval and navigation.

### Recommended Files in `memory_bank`

| File Name               | Purpose                                                        |
|-------------------------|----------------------------------------------------------------|
| activeContext.md        | Current working assumptions, focus areas, and priorities       |
| implementation-plan.md  | Step-by-step technical plan and architecture                   |
| productContext.md       | Product requirements, user needs, and business context         |
| progress.md             | Ongoing progress updates, milestones, blockers                 |
| projectbrief.md         | High-level summary and objectives of the project               |
| systemPatterns.md       | Design patterns, system architecture, reusable solutions       |
| task.md                 | Current and pending tasks, with status and ownership           |
| techContext.md          | Technical constraints, stack choices, integration notes        |

#### Example Structure

```
project-root/
  memory_bank/
    activeContext.md
    implementation-plan.md
    productContext.md
    progress.md
    projectbrief.md
    systemPatterns.md
    task.md
    techContext.md
```

- Curate memory banks to include only relevant, accurate, and up-to-date information.
- Document the purpose, scope, and intended audience for each memory bank.
- Ensure memory banks are accessible to relevant stakeholders for collaboration and onboarding.
- Regularly review shared memory banks for privacy and security, ensuring sensitive information is only accessible to authorized users.
- Track changes (e.g., via version control) and encourage feedback/contributions to improve quality and completeness.
- After every update or change to the project, promptly update the relevant documentation files in the `memory_bank` to reflect the latest state, decisions, and context.
- When analyzing or initializing a new project, create comprehensive and detailed documentation in all relevant `memory_bank` files to capture context, objectives, requirements, technical plans, and assumptions from the outset.

---
