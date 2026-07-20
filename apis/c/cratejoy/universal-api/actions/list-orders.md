# Cratejoy: List Orders

Retrieves orders from Cratejoy.

```
GET https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-orders?${params}`, {
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
      "customer_id": 1,
      "financial_status": "string",
      "fulfillment_status": "string",
      "gift_message": "string",
      "id": 1,
      "is_gift": true,
      "is_test": true,
      "placed_at": "2026-05-07T12:00:00.000Z",
      "total": 1,
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer_id` | number |  |
| `financial_status` | string |  |
| `fulfillment_status` | string |  |
| `gift_message` | string |  |
| `id` | number |  |
| `is_gift` | boolean |  |
| `is_test` | boolean |  |
| `placed_at` | date |  |
| `total` | number |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Cratejoy API, this operation is `GET /v1/orders/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

