# Maildrip: Execute an MCP tool



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/execute-an-mcp-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/execute-an-mcp-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/execute-an-mcp-tool', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the tool to execute |
| `arguments` | object | no | Arguments to pass to the tool (varies by tool) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {},
      "tool": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object | Tool execution result (varies by tool) |
| `tool` | string | Name of the executed tool |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/mcp/tools/call` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-an-mcp-tool.md) for the provider-specific parameters and requirements.

