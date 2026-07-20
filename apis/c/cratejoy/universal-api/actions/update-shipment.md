# Cratejoy: Update Shipment

Updates an existing shipment in Cratejoy.

```
PUT https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/update-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/update-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shipId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/update-shipment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shipId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipId` | number | yes | The Cratejoy shipment ID. |
| `adjustedOrderedAt` | string | no | The target ship date for the shipment. |
| `trackingNumber` | string | no | The tracking number for the shipment. |
| `status` | string | no | The shipment status. |
| `carrierName` | string | no | The shipment carrier name. |
| `trackingLink` | string | no | The tracking URL for the shipment. |
| `shippedAt` | string | no | The shipped timestamp for the shipment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adjusted_ordered_at": "2026-05-07T12:00:00.000Z",
      "customer_id": 1,
      "id": 1,
      "shipped_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "target_at": "2026-05-07T12:00:00.000Z",
      "tracking_number": "string",
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
| `adjusted_ordered_at` | date |  |
| `customer_id` | number |  |
| `id` | number |  |
| `shipped_at` | date |  |
| `status` | string |  |
| `target_at` | date |  |
| `tracking_number` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Cratejoy API, this operation is `PUT /v1/shipments/:shipId/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shipment.md) for the provider-specific parameters and requirements.

