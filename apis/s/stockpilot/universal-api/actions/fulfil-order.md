# Stockpilot: Fulfil Order

Updates an order as fulfilled in Stockpilot.

```
PUT https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/fulfil-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/fulfil-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/fulfil-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `carrierCode` | string | no |  |
| `items[].sku` | string | no |  |
| `orderPk` | number | no |  |
| `service` | string | no |  |
| `shipmentType` | string | no |  |
| `shippingMethod` | string | no |  |
| `orderNumber` | string | no |  |
| `fulfilledAt` | string | no |  |
| `carrierName` | string | no |  |
| `trackingCode` | string | no |  |
| `trackingUrl` | string | no | Default: `https://www.no-tracking-url.com/`. |
| `items[]` | array<object> | no |  |
| `items[].quantity` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed_at": "2026-05-07T12:00:00.000Z",
      "message": "string",
      "order_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed_at` | date |  |
| `message` | string |  |
| `order_id` | string |  |

## Native endpoint

Through the native Stockpilot API, this operation is `POST /orders/fulfil` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fulfil-order.md) for the provider-specific parameters and requirements.

