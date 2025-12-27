# Claude Code: Agentic CLI Tool & Skills

## Summary
Claude Code is an agentic command-line interface (CLI) tool by Anthropic that brings Claude's intelligence directly into the development environment. Unlike traditional autocomplete assistants, it operates autonomously to perform complex, multi-step engineering tasks. The standout feature is "Agent Skills" - reusable, modular workflows that teach the agent specialized tasks without overwhelming the context window. Claude Code shifts developers from typing code to orchestrating logic.

---

## Key Terms
- **Claude Code**: An agentic CLI tool developed by Anthropic that integrates Claude's AI capabilities into the terminal for autonomous development tasks
- **Agent Skills (Skills)**: A directory containing a SKILL.md file and optional resources that teaches Claude Code how to perform specialized tasks
- **Progressive Disclosure**: Design principle where only skill metadata is loaded at startup, with full instructions loaded only when activated
- **Context Window**: The amount of information/tokens the AI model can process at once
- **CLAUDE.md**: "Always-on" project memory file loaded in every session for persistent rules
- **Slash Commands**: Manually invoked macros for specific, repeatable prompts (e.g., /test)
- **Agentic**: Operating autonomously to complete multi-step tasks without constant user input

---

## How Skills Work

### Skill Structure
- A Skill is a directory containing:
  - `SKILL.md` file (instructions)
  - Optional supporting resources (scripts, templates, reference files)

### Triggering Mechanism
1. **Discovery**: Claude Code analyzes your request against available Skill descriptions
2. **Activation**: If a match is found, it reads the full SKILL.md and supporting files into context
3. **Execution**: Follows the structured workflow defined in the Skill

---

## Core Capabilities

### Deep Context Awareness
- Scans file system to understand project architecture
- Recognizes dependencies and style patterns

### Terminal Autonomy
- Executes terminal commands directly
- Runs tests, lints code, manages packages

### Git Integration
- Creates clean commits with descriptive messages
- Resolves merge conflicts

### Refactoring & Debugging
- Reads and explains complex legacy code
- Safely refactors while maintaining behavior

---

## Customization Hierarchy

| Level | Description | When Loaded |
|-------|-------------|-------------|
| **CLAUDE.md** | Always-on project memory (e.g., "Always use TypeScript") | Every session |
| **Slash Commands** | Manually invoked macros for repeatable prompts | On user command |
| **Skills** | Auto-discovered workflows for complex tasks | When intent matches |

---

## Review Questions

### Recall
1. What is Claude Code and how does it differ from traditional autocomplete assistants?
2. What is a Skill in Claude Code, and what files does it contain?
3. What is "Progressive Disclosure" and why is it important?
4. Name four core capabilities of Claude Code.
5. What is the purpose of CLAUDE.md?

### Application
1. You have a repetitive task of reviewing PRs for security issues. How would you use Skills to automate this?
2. Your team always uses TypeScript and follows specific coding conventions. Which customization mechanism would you use to enforce this across all sessions?

### Critical Thinking
1. Why might Progressive Disclosure be more effective than loading all skill instructions upfront? What trade-offs does this approach introduce?
2. How does the shift from "typing code" to "orchestrating logic" change the role of a software developer?

---

## Quick Reference

| Component | Purpose |
|-----------|---------|
| `SKILL.md` | Contains skill instructions |
| `CLAUDE.md` | Project-level always-on memory |
| `/command` | Slash command for manual invocation |

**Key Principle**: Skills = Auto-discovery + Context-efficient loading + Structured workflows
