# Brief: Call MCP Tool

Calls an MCP tool in Brief by name.

```
GET https://connect.mindcloud.co/v1/universal/brief/latest/actions/call-mcp-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brief `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Default: `tool-call`. |
| `mcpSessionId` | string | yes | Session id returned by Initialize MCP Session response header. |
| `params.arguments` | object | no | Default: `{}`. |
| `params.name` | string | yes |  |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[].text` | string |  |
| `content[].type` | string |  |

## Native endpoint

Through the native Brief API, this operation is `POST /mcp` (base URL `https://app.briefhq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/call-mcp-tool.md) for the provider-specific parameters and requirements.

