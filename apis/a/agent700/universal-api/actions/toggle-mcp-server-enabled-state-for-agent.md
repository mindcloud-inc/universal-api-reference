# Agent700: Toggle MCP Server Enabled State for Agent



```
PUT https://connect.mindcloud.co/v1/universal/agent700/latest/actions/toggle-mcp-server-enabled-state-for-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent700 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/agent700/latest/actions/toggle-mcp-server-enabled-state-for-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "serverName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agent700/latest/actions/toggle-mcp-server-enabled-state-for-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "serverName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes |  |
| `serverName` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agent700 API returns.

## Native endpoint

Through the native Agent700 API, this operation is `POST /agents/:agent_id/mcp/servers/:server_name/toggle` (base URL `https://api.agent700.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/toggle-mcp-server-enabled-state-for-agent.md) for the provider-specific parameters and requirements.

