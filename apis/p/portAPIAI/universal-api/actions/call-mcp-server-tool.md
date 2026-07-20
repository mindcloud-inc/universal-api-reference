# Port API AI: Call MCP Server Tool

Calls an MCP server tool in Port.

```
POST https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/call-mcp-server-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/call-mcp-server-tool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "serverId": "string",
  "toolName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/call-mcp-server-tool', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "serverId": "string",
    "toolName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `serverId` | string | yes | The Port MCP server identifier. |
| `toolName` | string | yes | The Port MCP tool name. |
| `arguments` | object | no | Arguments passed to the MCP tool. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `message` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /mcp/servers/:server_id/tools/:tool_name/call` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/call-mcp-server-tool.md) for the provider-specific parameters and requirements.

