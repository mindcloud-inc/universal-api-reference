# Stockpilot: List Orders

Retrieves orders from Stockpilot.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-orders?${params}`, {
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
| `status` | string | no |  |
| `isForwarded` | string | no | Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "current_page": 1,
      "next": true,
      "previous": true,
      "results": [
        [
          {}
        ]
      ],
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `current_page` | number |  |
| `next` | boolean |  |
| `previous` | boolean |  |
| `results[]` | array<object> |  |
| `results[].created_at` | date |  |
| `results[].customer_name` | string |  |
| `results[].id` | number |  |
| `results[].order_details.total` | string |  |
| `results[].order_number` | string |  |
| `results[].status` | string |  |
| `total_pages` | number |  |

## Native endpoint

Through the native Stockpilot API, this operation is `GET /orders` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

