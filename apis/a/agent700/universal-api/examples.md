# Agent700 Universal API Examples

These examples use the MindCloud API key and Agent700 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agents



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agent700/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agent700/latest/actions/list-agents?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Agents action reference](actions/list-agents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agent700/latest/actions/list-agents).

## Add MCP Server to Agent



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agent700/latest/actions/add-mcp-server-to-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agent700/latest/actions/add-mcp-server-to-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add MCP Server to Agent action reference](actions/add-mcp-server-to-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agent700/latest/actions/add-mcp-server-to-agent).
