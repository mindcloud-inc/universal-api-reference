# Brief: Initialize MCP Session

Creates an MCP session in Brief.

```
POST https://connect.mindcloud.co/v1/universal/brief/latest/actions/initialize-mcp-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brief `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Request identifier. Default: `initialize`. |
| `params.clientInfo.name` | string | yes | Client name for initialize. Default: `mindcloud`. |
| `params.clientInfo.version` | string | yes | Client version for initialize. Default: `1.0.0`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capabilities.tools.listChanged` | boolean |  |
| `protocolVersion` | string |  |
| `serverInfo.name` | string |  |
| `serverInfo.version` | string |  |

## Native endpoint

Through the native Brief API, this operation is `POST /mcp` (base URL `https://app.briefhq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initialize-mcp-session.md) for the provider-specific parameters and requirements.

