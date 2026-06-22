# Blank Project Template

A starter template for creating new projects in [Smartloop Studio](https://smartloop.ai). Use this as a foundation to build custom project templates or as-is to bootstrap a new project with sensible defaults.

## What's Included

This template ships with a minimal working setup:

- **System tools** — built-in file operations (`file-read`, `file-write`), shell access (`bash`), and codebase exploration (`explore`)
- **Fetch MCP server** — retrieves and extracts content from URLs as markdown
- **fetch-url skill** — a pre-configured skill that uses the fetch tool to extract information from any URL on demand

## Project Structure

```
├── workspace.json          # Workspace definition (project metadata, MCP servers, UI state)
├── manifest.json           # Full project manifest (tools, server configs, sessions)
├── workspace/
│   └── .workspace_manifest.json
├── project/
│   ├── mcp-smartloop.md    # Docs for built-in system tools
│   ├── mcp-fetch.md        # Docs for the fetch MCP server
│   └── skills/
│       └── fetch-url/
│           └── SKILL.md    # Skill definition for URL fetching
├── conversations/          # Conversation history (empty on init)
└── LICENSE                 # MIT
```

## Usage

### Creating a Project from This Template

1. Clone or download this repository
2. Import the `workspace.json` into Smartloop Studio, or copy the template directory into your Studio workspace location
3. Rename the project in `workspace.json` by updating the `project.name` field

### Extending the Template

**Add a new skill** — Create a directory under `project/skills/` with a `SKILL.md` file:

```
project/skills/my-skill/
└── SKILL.md
```

The `SKILL.md` uses frontmatter to define when the skill is triggered:

```markdown
---
name: my-skill
description: Use when the user asks to do X — performs Y.
---

Instructions for the skill go here.
```

**Add an MCP server** — Register the server in `workspace.json` under `mcp_servers` and add a corresponding documentation file in `project/` (e.g., `mcp-myserver.md`) describing its available tools and parameters.

**Add documents** — Place reference documents in the project directory and register them in `manifest.json` under `project.documents` to make them available as context during conversations.

## Creating Your Own Project Template

Fork this repository and customize it for your use case:

1. Add domain-specific skills to `project/skills/`
2. Configure additional MCP servers for the tools your workflow requires
3. Include starter documents or reference material
4. Update `workspace.json` with your preferred project name, color, and temperature settings

The resulting repository can be shared as a reusable template for anyone using Smartloop Studio.

## License

MIT
