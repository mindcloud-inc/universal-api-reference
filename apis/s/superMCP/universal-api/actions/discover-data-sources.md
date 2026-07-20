# SuperMCP: Discover Data Sources



```
GET https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/discover-data-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperMCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/discover-data-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/discover-data-sources?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `compress` | boolean | no | Return a compact TOON response instead of JSON when supported. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data_sources": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data_sources` | array<object> | Available Supermetrics data sources. |
| `total` | number | Number of returned data sources. |

## Native endpoint

Through the native SuperMCP API, this operation is `POST /mcp/data_source_discovery` (base URL `https://mcp.supermetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/discover-data-sources.md) for the provider-specific parameters and requirements.

