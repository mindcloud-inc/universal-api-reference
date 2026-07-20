# Brief: List MCP Tools

Retrieves available MCP tools from Brief.

```
GET https://connect.mindcloud.co/v1/universal/brief/latest/actions/list-mcp-tools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brief `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brief/latest/actions/list-mcp-tools?connectionId=$CONNECTION_ID&id=tools-list&mcpSessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "tools-list",
  "mcpSessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brief/latest/actions/list-mcp-tools?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Default: `tools-list`. |
| `mcpSessionId` | string | yes | Session id returned by Initialize MCP Session response header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tools": [
        {
          "annotations": {
            "readOnlyHint": true
          },
          "description": "string",
          "execution": {
            "taskSupport": "string"
          },
          "inputSchema": {
            "$schema": "string",
            "type": "string"
          },
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tools[].annotations.readOnlyHint` | boolean |  |
| `tools[].description` | string |  |
| `tools[].execution.taskSupport` | string |  |
| `tools[].inputSchema.$schema` | string |  |
| `tools[].inputSchema.type` | string |  |
| `tools[].name` | string |  |

## Native endpoint

Through the native Brief API, this operation is `POST /mcp` (base URL `https://app.briefhq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mcp-tools.md) for the provider-specific parameters and requirements.

