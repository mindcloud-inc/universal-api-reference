# Brief: Native API Reference

A consolidated summary of Brief's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://briefhq.ai/docs/mcp-setup/
- **API base URL:** `https://app.briefhq.ai`

## Authentication

### API Key

Authenticate using a Brief API key generated in Brief Settings > Integrations.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://briefhq.ai/docs/mcp-setup/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json, text/event-stream` |
| `content-type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Call MCP Tool](actions/call-mcp-tool.md) | `POST /mcp` | [docs](https://briefhq.ai/docs/mcp-setup/) |
| [Initialize MCP Session](actions/initialize-mcp-session.md) | `POST /mcp` | [docs](https://briefhq.ai/docs/mcp-setup/) |
| [List MCP Tools](actions/list-mcp-tools.md) | `POST /mcp` | [docs](https://briefhq.ai/docs/mcp-setup/) |
