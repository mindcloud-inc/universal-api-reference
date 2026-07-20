# YouCan: List Coupons

Retrieves a list of coupons from YouCan.

```
GET https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-coupons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-coupons?${params}`, {
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
| `limit` | string | no |  |
| `page` | string | no |  |
| `q` | string | no |  |
| `sort_field` | string | no |  |
| `sort_order` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "code": "string",
          "description": "string",
          "end_date": 1,
          "id": "string",
          "max_usage": 1,
          "start_date": 1,
          "status": "string",
          "type": 1,
          "type_text": "string",
          "value": 1
        }
      ],
      "meta": {
        "pagination": {
          "count": 1,
          "current_page": 1,
          "links": {},
          "per_page": 1,
          "total": 1,
          "total_pages": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].code` | string |  |
| `data[].description` | string |  |
| `data[].end_date` | number |  |
| `data[].id` | string |  |
| `data[].max_usage` | number |  |
| `data[].start_date` | number |  |
| `data[].status` | string |  |
| `data[].type` | number |  |
| `data[].type_text` | string |  |
| `data[].value` | number |  |
| `meta` | object |  |
| `meta.pagination` | object |  |
| `meta.pagination.count` | number |  |
| `meta.pagination.current_page` | number |  |
| `meta.pagination.links` | object |  |
| `meta.pagination.per_page` | number |  |
| `meta.pagination.total` | number |  |
| `meta.pagination.total_pages` | number |  |

## Native endpoint

Through the native YouCan API, this operation is `GET /coupons` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-coupons.md) for the provider-specific parameters and requirements.

