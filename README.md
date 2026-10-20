# KeelTools Directory — Open Catalog & MCP Manifest

Public metadata companion for [KeelTools](https://keeltools.com) (keeltools.com), a bilingual directory of AI tools, agent skills and prompts.

**What this repo is**: the open, machine-readable manifest behind the KeelTools MCP endpoint, published so directories and clients can pull structured metadata from GitHub. The full catalog and detail pages live on the website; this repository contains metadata only.

## Contents

| Path | What it is |
|---|---|
| [`server.json`](server.json) | MCP Registry manifest for the remote server `https://keeltools.com/mcp` (namespace `com.keeltools/keeltools-directory`). Streamable HTTP, read-only, no login required. |
| [`catalog.json`](catalog.json) | Compact public index of catalog entries: type (tool / skill / prompt), slug, detail-page URL. Metadata only — no proprietary content. |

## The MCP endpoint

- Transport: Streamable HTTP
- URL: `https://keeltools.com/mcp`
- Auth: none (public, read-only)
- Tools:
  - `search_directory` — search entries by name, alias or tagline; optional type filter (tool / skill / prompt)
  - `get_entry` — fetch one entry's detail by type and slug

Ready-to-paste client config:

```json
{
  "mcpServers": {
    "keeltools": { "type": "http", "url": "https://keeltools.com/mcp" }
  }
}
```

Setup guide, domain-auth details and FAQ: [keeltools.com/about](https://keeltools.com/about/).

## Official registry

The endpoint is published in the official Model Context Protocol Registry as `com.keeltools/keeltools-directory`.

## License

Catalog metadata in this repository is provided for indexing and reference. Tool names and descriptions belong to their respective owners.
