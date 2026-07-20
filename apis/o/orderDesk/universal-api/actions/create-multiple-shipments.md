# Order Desk: Create Multiple Shipments

Creates multiple shipments in Order Desk.

```
POST https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/create-multiple-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/create-multiple-shipments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shipments[].orderId": "string",
  "shipments[].trackingNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/create-multiple-shipments', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shipments[].orderId": "string",
    "shipments[].trackingNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipments[].orderId` | string | yes | Order Desk internal order ID for the shipment target. |
| `shipments[].trackingNumber` | string | yes | Carrier tracking number for the shipment. |
| `shipments[].carrierCode` | string | no | Carrier code such as UPS or USPS. |
| `shipments[].shipmentMethod` | string | no | Shipment service or method label. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": "string",
      "message": "string",
      "results": [
        {}
      ],
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
| `results` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Order Desk API, this operation is `POST /batch-shipments` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-multiple-shipments.md) for the provider-specific parameters and requirements.

