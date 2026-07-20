# Agent700: Add MCP Server to Agent



```
POST https://connect.mindcloud.co/v1/universal/agent700/latest/actions/add-mcp-server-to-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent700 `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agent700 API returns.

## Native endpoint

Through the native Agent700 API, this operation is `POST /agents/:agent_id/mcp/servers` (base URL `https://api.agent700.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-mcp-server-to-agent.md) for the provider-specific parameters and requirements.

