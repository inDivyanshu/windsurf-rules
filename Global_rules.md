# Global Rules for Cascade AI Coding Assistant

These guidelines are for Cascade, a coding assistant, to ensure all generated code and interactions are consistent, clear, and maintainable across all languages and projects. Always apply these principles to produce clean, understandable, and efficient code.

## Best Practices
- Explain the “why” behind major changes  
- Self-review each result  
- Record key context in memory  
- Keep docs up-to-date; note rationale  
- Combine related edits into one commit  
- Add/update tests for new features or fixes  
- One-line English commit messages  

## Style & Readability
- Favor clarity over cleverness  
- Consistent naming (snake_case, camelCase)  
- Enforce formatting with linters/formatters  
- Comments explain intent, not restate code  
- Small, single-responsibility functions  

## Architecture & Modularity
- Encapsulate complexity behind clear APIs  
- Decouple via interfaces/DI  
- DRY: factor out repetition  

## Error Handling & Testing
- Fail fast with clear errors  
- Design for testability; separate pure logic  
- Validate inputs early  

## Performance & Resources
- Use appropriate data structures/algorithms  
- Avoid premature optimization  
- Manage handles (files, connections) responsibly  

## Commit Messages
One-line English message with prefix:
`feat, fix, tweak, style, refactor, perf, test, docs, chore, ci, build, revert, hotfix, init, merge, wip, release`

## Memory Bank
Place docs in `memory_bank/`:
- activeContext.md  
- implementation-plan.md  
- productContext.md  
- progress.md  
- projectbrief.md  
- systemPatterns.md  
- task.md  
- techContext.md  

_Update memory files after each change._
