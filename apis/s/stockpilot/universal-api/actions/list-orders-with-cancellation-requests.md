# Stockpilot: List Orders with Cancellation Requests

Retrieves orders with cancellation requests from Stockpilot.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-orders-with-cancellation-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-orders-with-cancellation-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-orders-with-cancellation-requests?${params}`, {
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
| `total_pages` | number |  |

## Native endpoint

Through the native Stockpilot API, this operation is `GET /orders/cancellation-requests` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders-with-cancellation-requests.md) for the provider-specific parameters and requirements.

