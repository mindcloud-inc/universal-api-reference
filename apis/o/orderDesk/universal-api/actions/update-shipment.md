# Order Desk: Update Shipment

Updates an existing shipment in Order Desk.

```
PUT https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/update-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/update-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string",
  "shipmentId": "string",
  "trackingNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/update-shipment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string",
    "shipmentId": "string",
    "trackingNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | string | yes | Order Desk internal order ID. |
| `shipmentId` | string | yes | Order Desk internal shipment ID. |
| `trackingNumber` | string | yes | Carrier tracking number for the shipment. |
| `carrierCode` | string | no | Carrier code such as UPS or USPS. |
| `shipmentMethod` | string | no | Shipment service or method label. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `executionTime` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Order Desk API, this operation is `PUT /orders/:orderId/shipments/:shipmentId` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shipment.md) for the provider-specific parameters and requirements.

