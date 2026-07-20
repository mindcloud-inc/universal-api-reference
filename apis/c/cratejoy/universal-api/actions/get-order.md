# Cratejoy: Get Order

Retrieves an order from Cratejoy.

```
GET https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/get-order?connectionId=$CONNECTION_ID&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/get-order?${params}`, {
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
| `orderId` | number | yes | The Cratejoy order ID. |

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

Through the native Cratejoy API, this operation is `GET /v1/orders/:orderId/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

