# <img src="https://images.mindcloud.co/apps/icons/brief_1775139591994.png" alt="Brief logo" width="28" height="28"> Brief: Universal API

Brief is an AI product-context platform that connects product, engineering, and customer tools so teams and coding agents can retrieve decisions, docs, signals, and strategic context.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/brief/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://briefhq.ai/
- **Vendor API docs:** https://briefhq.ai/docs/mcp-setup/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Call MCP Tool](actions/call-mcp-tool.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brief/latest/actions/call-mcp-tool?connectionId=$CONNECTION_ID&id=tool-call&mcpSessionId=string&params.name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Mcp

| Action | Method | Description |
| --- | --- | --- |
| [Call MCP Tool](actions/call-mcp-tool.md) | GET | Calls an MCP tool in Brief by name. |
| [Initialize MCP Session](actions/initialize-mcp-session.md) | POST | Creates an MCP session in Brief. |
| [List MCP Tools](actions/list-mcp-tools.md) | GET | Retrieves available MCP tools from Brief. |

