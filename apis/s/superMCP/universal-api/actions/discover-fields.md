# SuperMCP: Discover Fields



```
GET https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/discover-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperMCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/discover-fields?connectionId=$CONNECTION_ID&dataSourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataSourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/discover-fields?${params}`, {
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
| `dataSourceId` | string | yes | Supermetrics data source ID to inspect fields for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Optional field filter string. |
| `compress` | boolean | no | Return a compact TOON response instead of JSON when supported. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data_source": "string",
      "dimensions": [
        {}
      ],
      "metrics": [
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
| `data_source` | string | Data source ID. |
| `dimensions` | array<object> | Available dimensions. |
| `metrics` | array<object> | Available metrics. |
| `total` | number | Total fields returned. |

## Native endpoint

Through the native SuperMCP API, this operation is `POST /mcp/field_discovery` (base URL `https://mcp.supermetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/discover-fields.md) for the provider-specific parameters and requirements.

