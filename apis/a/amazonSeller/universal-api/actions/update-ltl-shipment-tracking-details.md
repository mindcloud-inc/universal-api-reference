# Amazon Seller: Update LTL Shipment Tracking Details

Updates LTL shipment tracking details in Amazon Seller.

```
PUT https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/update-ltl-shipment-tracking-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/update-ltl-shipment-tracking-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboundPlanId": "string",
  "shipmentId": "string",
  "freightBillNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/update-ltl-shipment-tracking-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboundPlanId": "string",
    "shipmentId": "string",
    "freightBillNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboundPlanId` | string | yes | Identifier of an inbound plan. |
| `shipmentId` | string | yes | Identifier of a shipment. A shipment contains the boxes and units being inbounded. |
| `freightBillNumber` | string | yes | Number associated with the freight bill. (required: 1 \| max: 1) Accepts multiple values as an array. |
| `billOfLadingNumber` | string | no | The number of the carrier shipment acknowledgement document. (max length between 1 and 1024) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "operationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `operationId` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `POST inbound/fba/2024-03-20/inboundPlans/:inboundPlanId/shipments/:shipmentId/trackingDetails` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ltl-shipment-tracking-details.md) for the provider-specific parameters and requirements.

