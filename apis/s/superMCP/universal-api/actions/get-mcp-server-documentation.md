# SuperMCP: Get MCP Server Documentation



```
GET https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-mcp-server-documentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperMCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-mcp-server-documentation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-mcp-server-documentation?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "format": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Documentation content. |
| `format` | string | Documentation format. |
| `title` | string | Documentation title. |

## Native endpoint

Through the native SuperMCP API, this operation is `GET /mcp/resources/docs` (base URL `https://mcp.supermetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mcp-server-documentation.md) for the provider-specific parameters and requirements.

