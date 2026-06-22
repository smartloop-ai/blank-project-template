# __system_mcp__

Built-in tools for file operations, search, and shell commands.

## Available Tools

### `bash`
Execute a shell command (git, echo, etc.) on the host machine

**Parameters:**
- `command` *(required)*: Shell command to execute

### `file-read`
Read a file and return its content

**Parameters:**
- `path` *(required)*: File path to read

### `file-write`
Write content to a file in the working directory

**Parameters:**
- `path` *(required)*: File path to write
- `content` *(required)*: Content to write

### `explore`
Explore the local project directory, read files, and produce an LLM-enriched summary of the codebase

**Parameters:**
- `query` *(required)*: What to look for in the codebase

**Parameters:**
- `name` *(required)*: Project name
- `description`: Project description

### `create-skill`
Create a new skill in the current project

**Parameters:**
- `name` *(required)*: Skill name
- `description`: Skill description
- `content` *(required)*: Skill content/instructions
