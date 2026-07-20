# Amazon Seller: Update SPD Shipment Tracking Details

Updates SPD shipment tracking details in Amazon Seller.

```
PUT https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/update-spd-shipment-tracking-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/update-spd-shipment-tracking-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboundPlanId": "string",
  "shipmentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/update-spd-shipment-tracking-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboundPlanId": "string",
    "shipmentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboundPlanId` | string | yes | Identifier of an inbound plan. |
| `ltlTrackingDetail.billOfLadingNumber` | string | no | The number of the carrier shipment acknowledgement document. (max length between 1 and 1024) |
| `shipmentId` | string | yes | Identifier of a shipment. A shipment contains the boxes and units being inbounded. |
| `spdTrackingItems[]` | array<object> | no | List of Small Parcel Delivery (SPD) tracking items. |
| `spdTrackingItems[].boxId` | string | no | The ID provided by Amazon that identifies a given box. This ID is comprised of the external shipment ID (which is generated after transportation has been confirmed) and the index of the box. |
| `ltlTrackingDetail` | object | no | Contains input information to update Less-Than-Truckload (LTL) tracking information. |
| `ltlTrackingDetail.freightBillNumber` | string | no | (required when shipping LTL) Number associated with the freight bill. Accepts multiple values as an array. |
| `spdTrackingItems[].trackingID` | string | no | The tracking ID associated with each box in a non-Amazon partnered Small Parcel Delivery (SPD) shipment. The seller must provide this information. |

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

Through the native Amazon Seller API, this operation is `POST inbound/fba/2024-03-20/inboundPlans/:inboundPlanId/shipments/:shipmentId/trackingDetails` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-spd-shipment-tracking-details.md) for the provider-specific parameters and requirements.

