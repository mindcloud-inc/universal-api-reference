# 2Smart Cloud: List dashboards



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-vendor-dashboards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-vendor-dashboards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-vendor-dashboards?${params}`, {
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
| `id[]` | array<number> | no | IDs of entities |
| `title` | string | no | Dashboard title |
| `is_enabled` | boolean | no | Whether the dashboard is enabled |
| `product_id` | number | no | Product identifier |
| `sort` | string | no | Dashboard sort field |
| `search` | string | no | Search for entity |
| `is_archived` | boolean | no | Is this entity archived |
| `order` | string | no | Sort order |
| `updated_from` | date | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `updated_to` | date | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_from` | date | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_to` | date | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `limit` | number | no | The number of rows to return |
| `offset` | number | no | Pagination offset |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Dashboard results |
| `meta` | object | Pagination metadata |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /vendor/dashboards` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vendor-dashboards.md) for the provider-specific parameters and requirements.

