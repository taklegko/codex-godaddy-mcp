---
name: godaddy-domains
description: Use GoDaddy's read-only Domains MCP endpoint to check domain availability and generate domain suggestions.
---

# GoDaddy Domains

Use this skill when the user wants to:

- Check whether one or more domain names are available.
- Generate domain name ideas from keywords, product descriptions, company descriptions, or naming constraints.
- Compare domain options by availability and fit.

The bundled MCP server is GoDaddy's public Domains MCP endpoint:

- URL: `https://api.godaddy.com/v1/domains/mcp`
- Transport: `streamable-http`
- Server name: `godaddy-domains`

## Safety And Scope

This plugin is read-only. Use it for domain search, availability checks, and suggestions only.

Do not claim that Codex can buy domains, reserve domains, update DNS, inspect GoDaddy account data, or perform account-specific actions through this plugin. If the user wants to register a domain or change DNS, tell them to complete that in GoDaddy or another registrar outside Codex.

No GoDaddy API key is required for the read-only MCP endpoint.

## Prompting Guidance

For exact availability checks, pass the requested domain name or names directly to the MCP tool.

For ideation, preserve the user's business context and constraints. Useful constraints include preferred TLDs, tone, length, keywords to include or avoid, and whether the name should sound technical, premium, playful, local, or broad.

Example user requests:

- "Check whether example.ai is available."
- "Find domain ideas for a privacy-first analytics product."
- "Suggest short `.com` domains for an indie macOS utility."
- "Compare these options: crispforge.com, crispforge.io, getcrispforge.com."
