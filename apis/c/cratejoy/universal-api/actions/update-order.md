# Cratejoy: Update Order

Updates an existing order in Cratejoy.

```
PUT https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/update-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | yes | The Cratejoy order ID. |
| `note` | string | no | A note for the order. |

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
| `placed_at` | date |  |
| `total` | number |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Cratejoy API, this operation is `PUT /v1/orders/:orderId/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.

