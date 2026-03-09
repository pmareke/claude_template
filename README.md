# Claude Code Project Template

A modular repository structure designed for building Claude Code projects with structured AI context, reusable skills, and automated development workflows.

## Overview

This template provides an opinionated structure for organizing Claude Code projects that:

- **Maintains AI context efficiently** through modular CLAUDE.md files
- **Enables reusable workflows** via skills for common development tasks
- **Automates quality checks** using hooks for consistent development practices
- **Separates concerns** between documentation, tooling, and application code

## Structure

```
claude_code_project/
├── CLAUDE.md                    # Root AI context and project guidance
├── README.md                    # Human-readable project documentation
├── docs/
│   ├── architecture.md          # System architecture documentation
│   ├── decisions/               # Architecture Decision Records (ADRs)
│   └── runbooks/                # Operational guides
├── .claude/
│   ├── settings.json            # Claude-specific configuration
│   ├── hooks/                   # Automation and quality checks
│   └── skills/                  # Reusable AI workflows
│       ├── code-review/
│       ├── refactor/
│       └── release/
├── tools/
│   ├── scripts/                 # Development automation scripts
│   └── prompts/                 # Reusable prompt templates
└── src/                         # Application source code
    ├── api/
    │   └── CLAUDE.md            # Module-specific context
    └── persistence/
        └── CLAUDE.md
```

## Getting Started

### Using This Template

1. **Clone or fork this repository**
   ```bash
   git clone <repository-url>
   cd claude_code_project
   ```

2. **Customize for your project**
   - Update `CLAUDE.md` with project-specific guidance
   - Replace this README with your project description
   - Define your architecture in `docs/architecture.md`

3. **Configure Claude settings**
   - Adjust `.claude/settings.json` as needed
   - Add project-specific hooks in `.claude/hooks/`
   - Create skills for repeated workflows in `.claude/skills/`

4. **Build your application**
   - Organize code in `src/` by functional domains
   - Add module-specific `CLAUDE.md` files for complex modules
   - Document architectural decisions in `docs/decisions/`

## Key Concepts

### CLAUDE.md Files

- **Root level**: High-level architecture, common commands, design principles
- **Module level**: Context specific to individual modules or subsystems
- **Purpose**: Provide Claude Code with non-obvious insights that improve productivity

### Skills

Reusable AI workflows for repeated development tasks:
- Located in `.claude/skills/`
- Each skill has a `SKILL.md` defining the workflow
- Examples: code review, refactoring, release management

### Hooks

Automated checks and guardrails:
- Located in `.claude/hooks/`
- Execute on specific events (e.g., pre-commit)
- Ensure consistency and quality

### Documentation

- **docs/architecture.md**: System design and component relationships
- **docs/decisions/**: Record significant architectural choices (ADRs)
- **docs/runbooks/**: Operational procedures and troubleshooting

## Design Principles

1. **Modular AI Context**: Keep CLAUDE.md files focused and scoped
2. **Reusable Workflows**: Extract patterns into skills
3. **Automated Quality**: Use hooks for consistency
4. **Document Decisions**: Capture architectural choices as they emerge
5. **Minimal Precise Context**: Provide only what's non-obvious and helpful

## Contributing

When contributing to projects using this template:

1. Read the root `CLAUDE.md` for project-specific guidance
2. Follow existing architectural patterns documented in `docs/`
3. Update module-specific `CLAUDE.md` files when adding complexity
4. Document significant decisions in `docs/decisions/`

## License

[Add your license here]

## Credits

Template structure by Brij Kishore Pandey
