# 2Smart Cloud: List products



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-admin-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-admin-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-admin-products?${params}`, {
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
| `title` | string | no | Title name of product |
| `search` | string | no | Search for entity |
| `is_archived` | boolean | no | Is this entity archived |
| `is_approved` | boolean | no | Is this product approved |
| `is_show_market` | boolean | no | Is this product shown in market |
| `status[]` | array<string> | no | Product status |
| `sort` | string | no | Sort key |
| `type` | string | no | Type of product |
| `abbreviation` | number | no | Abbreviation of product |
| `order` | string | no | Sort order |
| `updated_from` | string | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `updated_to` | string | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_from` | string | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_to` | string | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
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
| `data` | array<object> |  |
| `meta` | object |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /admin/products` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-admin-products.md) for the provider-specific parameters and requirements.

