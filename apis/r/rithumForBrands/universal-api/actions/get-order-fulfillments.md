# Rithum for Brands: Get Order Fulfillments

Retrieve all fulfillments for a specified order.

```
GET https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/get-order-fulfillments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/get-order-fulfillments?connectionId=$CONNECTION_ID&orderID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/get-order-fulfillments?${params}`, {
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
| `orderID` | string | yes | The Rithum-generated unique identifier for the order you want to see fulfillments for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelReturnLabelFormat": {},
      "createdDateUtc": "string",
      "deliveryStatus": "string",
      "distributionCenterID": 1,
      "earliestDeliveryDateUtc": {},
      "earliestShipDateUtc": {},
      "estimatedDeliveryDateUtc": {},
      "estimatedShipDateUtc": {},
      "externalFulfillmentCenterCode": {},
      "externalFulfillmentNumber": {},
      "externalFulfillmentReferenceNumber": {},
      "externalFulfillmentStatus": "string",
      "hasChannelPackingSlip": true,
      "hasChannelReturnLabel": true,
      "hasReturnLabel": true,
      "hasShippingLabel": true,
      "id": 1,
      "insuranceCost": 1,
      "labelFormat": {},
      "orderID": 1,
      "profileID": 1,
      "returnLabelFormat": {},
      "returnTrackingNumber": {},
      "sellerFulfillmentID": "string",
      "serialShippingContainerCode": {},
      "shippedDateUtc": "string",
      "shippingCarrier": "string",
      "shippingClass": "string",
      "shippingCost": 1,
      "shippingLabelRequestID": {},
      "stagingLocation": {},
      "taxCost": 1,
      "trackingNumber": "string",
      "trackingUrl": "https://example.com",
      "type": "string",
      "updatedDateUtc": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelReturnLabelFormat` | object |  |
| `createdDateUtc` | string |  |
| `deliveryStatus` | string |  |
| `distributionCenterID` | number |  |
| `earliestDeliveryDateUtc` | object |  |
| `earliestShipDateUtc` | object |  |
| `estimatedDeliveryDateUtc` | object |  |
| `estimatedShipDateUtc` | object |  |
| `externalFulfillmentCenterCode` | object |  |
| `externalFulfillmentNumber` | object |  |
| `externalFulfillmentReferenceNumber` | object |  |
| `externalFulfillmentStatus` | string |  |
| `hasChannelPackingSlip` | boolean |  |
| `hasChannelReturnLabel` | boolean |  |
| `hasReturnLabel` | boolean |  |
| `hasShippingLabel` | boolean |  |
| `id` | number |  |
| `insuranceCost` | number |  |
| `labelFormat` | object |  |
| `orderID` | number |  |
| `profileID` | number |  |
| `returnLabelFormat` | object |  |
| `returnTrackingNumber` | object |  |
| `sellerFulfillmentID` | string |  |
| `serialShippingContainerCode` | object |  |
| `shippedDateUtc` | string |  |
| `shippingCarrier` | string |  |
| `shippingClass` | string |  |
| `shippingCost` | number |  |
| `shippingLabelRequestID` | object |  |
| `stagingLocation` | object |  |
| `taxCost` | number |  |
| `trackingNumber` | string |  |
| `trackingUrl` | string |  |
| `type` | string |  |
| `updatedDateUtc` | string |  |

## Native endpoint

Through the native Rithum for Brands API, this operation is `GET Orders(:orderID)/Fulfillments` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-fulfillments.md) for the provider-specific parameters and requirements.

