# Extensiv Order Manager: Create External Shipment

Creates an external shipment in Extensiv Order Manager.

```
POST https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/create-external-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extensiv Order Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/create-external-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shipments[].shipMethod.shippingCarrier": "string",
  "shipments[].trackingNumber": "string",
  "shipments[].shipMethod": {},
  "shipments[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/create-external-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shipments[].shipMethod.shippingCarrier": "string",
    "shipments[].trackingNumber": "string",
    "shipments[].shipMethod": {},
    "shipments[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notifyCustomer` | boolean | no |  |
| `shipments[].carrierFee.amount` | number | no |  |
| `shipments[].shipMethod.shippingCarrier` | string | yes |  |
| `shipments[].trackingNumber` | string | yes |  |
| `shipments[].carrierFee.currency` | string | no |  |
| `shipments[].shipMethod` | object | yes |  |
| `shipments[].shipMethod.packageTypeId` | number | no |  |
| `updateChannel` | boolean | no |  |
| `shipments[]` | array<object> | yes |  |
| `shipments[].carrierFee` | object | no |  |
| `shipments[].shipMethod.shippingServiceId` | number | no |  |
| `shipments[].deliveryStatus` | list<string> | no |  |
| `shipments[].estimatedArrival` | string | no |  |
| `shipments[].insuranceTrackingNumber` | string | no |  |
| `shipments[].orderId` | number | no |  |
| `shipments[].orderNumber` | string | no |  |
| `shipments[].received` | string | no |  |
| `shipments[].salesChannelId` | string | no |  |
| `shipments[].shipDate` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order": {},
      "orderBatchNumber": 1,
      "processingMessage": "string",
      "shipment": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `order` | object | Order identifier object. |
| `orderBatchNumber` | number | Order batch number. |
| `processingMessage` | string | Processing message. |
| `shipment` | object | Created shipment object. |
| `status` | string | Shipment processing status. |

## Native endpoint

Through the native Extensiv Order Manager API, this operation is `PUT /v1.1/shipment/external` (base URL `https://api.skubana.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-external-shipment.md) for the provider-specific parameters and requirements.

