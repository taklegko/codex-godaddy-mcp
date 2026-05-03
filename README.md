# GoDaddy Domains MCP for Codex

Community Codex plugin wrapper around GoDaddy's public Domains MCP endpoint.

Use it in Codex to check domain availability and generate domain ideas without adding API keys or running a local MCP server.

This repository is not an official GoDaddy repository or official GoDaddy Codex plugin. It only packages GoDaddy's public read-only MCP endpoint for Codex marketplace installation.

## Install

Add this marketplace to Codex:

```bash
codex plugin marketplace add taklegko/codex-godaddy-mcp
```

Then open Codex plugin settings, install **GoDaddy Domains**, and enable it for your workspace.

## What It Does

- Checks availability for one or more domains.
- Suggests domains from keywords or product descriptions.
- Helps compare naming options.

Read-only limits:

- No domain purchases.
- No DNS changes.
- No GoDaddy account access.
- No account-specific actions.

The bundled MCP server points to:

```json
{
  "godaddy-domains": {
    "url": "https://api.godaddy.com/v1/domains/mcp",
    "transport": "streamable-http"
  }
}
```

## Example Prompts

- "Check if crispforge.com is available."
- "Find domain ideas for a privacy-first analytics product."
- "Suggest short `.com` domains for an indie macOS utility."
- "Compare these options: crispforge.com, crispforge.io, getcrispforge.com."

## Plugin Contents

- `.agents/plugins/marketplace.json`
- `plugins/godaddy-domains/.codex-plugin/plugin.json`
- `plugins/godaddy-domains/.mcp.json`
- `plugins/godaddy-domains/skills/godaddy-domains/SKILL.md`

## Privacy

This wrapper does not add its own backend, database, tracking script, or secret storage. Domain queries are sent by Codex to GoDaddy's public Domains MCP endpoint.

## Terms

This project is provided as an MIT-licensed community wrapper. GoDaddy's endpoint, services, and public APIs are governed by GoDaddy's own terms and policies.

## Links

- [GoDaddy Domains MCP article](https://www.godaddy.com/resources/news/inside-the-godaddy-domains-mcp-server)
- [OpenAI Codex plugin docs](https://developers.openai.com/codex/plugins/build)
- [Model Context Protocol](https://modelcontextprotocol.io/)

## License

MIT
