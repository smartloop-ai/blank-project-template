# fetch-mcp

The fetch mcp server is designed to retrieve and extract content from URLs, primarily in the form of markdown. It provides a ‘fetch’ tool that fetches data from the internet and presents it as markdown text.

## Available Tools

### `fetch`
Fetches a URL from the internet and extracts its contents as markdown

**Parameters:**
- `url` *(required)*: URL to fetch
- `max_length`: Maximum number of characters to return
- `start_index`: Start content from this character index
- `raw`: Get raw content without markdown conversion
