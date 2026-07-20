# Brief Universal API Examples

These examples use the MindCloud API key and Brief connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Call MCP Tool

Calls an MCP tool in Brief by name.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brief/latest/actions/call-mcp-tool?connectionId=$CONNECTION_ID&id=tool-call&mcpSessionId=string&params.name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "tool-call",
  "mcpSessionId": "string",
  "params.name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brief/latest/actions/call-mcp-tool?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {
          "text": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Call MCP Tool action reference](actions/call-mcp-tool.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/brief/latest/actions/call-mcp-tool).

## Initialize MCP Session

Creates an MCP session in Brief.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brief/latest/actions/initialize-mcp-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "initialize",
  "params.clientInfo.name": "mindcloud",
  "params.clientInfo.version": "1.0.0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brief/latest/actions/initialize-mcp-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "initialize",
    "params.clientInfo.name": "mindcloud",
    "params.clientInfo.version": "1.0.0"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "capabilities": {
        "tools": {
          "listChanged": true
        }
      },
      "protocolVersion": "string",
      "serverInfo": {
        "name": "Ava Chen",
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Initialize MCP Session action reference](actions/initialize-mcp-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/brief/latest/actions/initialize-mcp-session).
