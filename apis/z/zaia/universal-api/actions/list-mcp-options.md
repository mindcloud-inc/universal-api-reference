# Zaia: List MCP Options

Retrieves MCP options from your Zaia workspace.

```
GET https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-mcp-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zaia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-mcp-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zaia/latest/actions/list-mcp-options?${params}`, {
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
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `type` | string | Available MCP toolkit type. |

## Native endpoint

Through the native Zaia API, this operation is `GET /api/v1/mcps/options` (base URL `https://api.endless.zaia.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mcp-options.md) for the provider-specific parameters and requirements.

