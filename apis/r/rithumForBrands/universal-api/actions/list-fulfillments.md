# Rithum for Brands: List Fulfillments

Retrieve existing Fulfillments.

```
GET https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-fulfillments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-fulfillments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/list-fulfillments?${params}`, {
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
| `fullfillmentID` | string | no | (optional) A Rithum generated unique identifier for a specific Fulfillment. |
| `filter` | string | no | (optional) Use a custom filter. (*oData*). **Examples**: - OrderID eq 20008076 - CreatedDateUtc ge 2016-03-02 and CreatedDateUtc lt 2016-03-03 |
| `expand` | list<string> | no | (optional) Expand a specific sublist (i.e. Items on this Fulfillment.) |

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
      "items": [
        {
          "distributionCenterCalculatedItemUnitCost": {},
          "distributionCenterCalculatedShippingCost": {},
          "distributionCenterItemUnitCost": {},
          "distributionCenterShippingCost": {},
          "fulfillmentID": 1,
          "id": 1,
          "marketplaceShippingStatus": "string",
          "orderID": 1,
          "orderItemID": 1,
          "productID": 1,
          "profileID": 1,
          "quantity": 1,
          "referenceProductID": {},
          "referenceSku": {},
          "sellerFulfillmentItemID": {},
          "sku": "string",
          "warehouseLocation": {}
        }
      ],
      "labelFormat": {},
      "orderID": 1,
      "profileID": 1,
      "returnLabelFormat": {},
      "returnTrackingNumber": {},
      "sellerFulfillmentID": {},
      "serialShippingContainerCode": {},
      "shippedDateUtc": {},
      "shippingCarrier": "string",
      "shippingClass": "string",
      "shippingCost": 1,
      "shippingLabelRequestID": {},
      "stagingLocation": {},
      "taxCost": 1,
      "trackingNumber": {},
      "trackingUrl": {},
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
| `items[].distributionCenterCalculatedItemUnitCost` | object |  |
| `items[].distributionCenterCalculatedShippingCost` | object |  |
| `items[].distributionCenterItemUnitCost` | object |  |
| `items[].distributionCenterShippingCost` | object |  |
| `items[].fulfillmentID` | number |  |
| `items[].id` | number |  |
| `items[].marketplaceShippingStatus` | string |  |
| `items[].orderID` | number |  |
| `items[].orderItemID` | number |  |
| `items[].productID` | number |  |
| `items[].profileID` | number |  |
| `items[].quantity` | number |  |
| `items[].referenceProductID` | object |  |
| `items[].referenceSku` | object |  |
| `items[].sellerFulfillmentItemID` | object |  |
| `items[].sku` | string |  |
| `items[].warehouseLocation` | object |  |
| `labelFormat` | object |  |
| `orderID` | number |  |
| `profileID` | number |  |
| `returnLabelFormat` | object |  |
| `returnTrackingNumber` | object |  |
| `sellerFulfillmentID` | object |  |
| `serialShippingContainerCode` | object |  |
| `shippedDateUtc` | object |  |
| `shippingCarrier` | string |  |
| `shippingClass` | string |  |
| `shippingCost` | number |  |
| `shippingLabelRequestID` | object |  |
| `stagingLocation` | object |  |
| `taxCost` | number |  |
| `trackingNumber` | object |  |
| `trackingUrl` | object |  |
| `type` | string |  |
| `updatedDateUtc` | string |  |

## Native endpoint

Through the native Rithum for Brands API, this operation is `GET Fulfillments(:fullfillmentID)` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fulfillments.md) for the provider-specific parameters and requirements.

