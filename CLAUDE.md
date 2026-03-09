# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a template repository for structuring Claude Code projects. It provides a modular architecture designed for building projects with:
- Structured AI context and project memory
- Reusable skills for AI workflows
- Automated development workflows via hooks
- Clear separation between documentation, tooling, and source code

## Repository Structure

### Core Components

**CLAUDE.md** (root and per-module)
- Root CLAUDE.md: High-level project guidance, architecture, common commands
- Module-specific CLAUDE.md (e.g., `src/api/CLAUDE.md`): Context specific to that module
- Keep focused on non-obvious architecture and patterns that require multiple files to understand
- Update when architectural patterns emerge or change

**.claude/skills/**
- Reusable AI workflows organized by purpose:
  - `code-review/SKILL.md`: Code review processes
  - `refactor/SKILL.md`: Refactoring workflows
  - `release/SKILL.md`: Release preparation and execution
- Each skill contains a SKILL.md file with the workflow definition
- Create new skills for repeated workflows that benefit from consistent execution

**.claude/hooks/**
- Guardrails and automation checks that run on specific events
- Examples: pre-commit validation, test runners, linting enforcement
- Use for quality gates and automated checks

**.claude/settings.json**
- Claude-specific project configuration
- Currently minimal but can be extended for project-specific settings

**docs/**
- `architecture.md`: High-level architecture documentation
- `decisions/`: Architecture Decision Records (ADRs)
- `runbooks/`: Operational procedures and troubleshooting guides
- Document significant decisions and non-obvious architectural patterns

**tools/**
- `scripts/`: Development and automation scripts
- `prompts/`: Reusable prompt templates for AI workflows

**src/**
- Core application modules
- Each module can have its own CLAUDE.md for module-specific context
- Organize by functional domain (e.g., `api/`, `persistence/`)

## Working with This Template

When using this template for a new project:

1. **Customize root CLAUDE.md**: Replace this template description with project-specific guidance
2. **Define architecture**: Document the system architecture in `docs/architecture.md`
3. **Create skills**: Add reusable workflows in `.claude/skills/` for common tasks
4. **Set up hooks**: Configure automation in `.claude/hooks/` for quality checks
5. **Structure source code**: Organize `src/` by functional domains, adding module-specific CLAUDE.md files where helpful

## Design Principles

- **Modular AI context**: Keep CLAUDE.md files focused; use module-specific files rather than one monolithic document
- **Reusable workflows**: Extract repeated patterns into skills
- **Automated quality**: Use hooks for consistency and quality gates
- **Documentation as decisions emerge**: Don't document prematurely; capture patterns as they stabilize
- **Minimal but precise context**: Provide only non-obvious information that aids productivity
