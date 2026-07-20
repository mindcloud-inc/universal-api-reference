# Amazon Seller: Get Marketplace Participations

Retrieves marketplace participations from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-marketplace-participations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-marketplace-participations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-marketplace-participations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amazonOrderId": "string",
      "automatedShippingSettings": {
        "automatedCarrier": "string",
        "automatedCarrierName": "Ava Chen",
        "automatedShipMethod": "string",
        "automatedShipMethodName": "Ava Chen",
        "hasAutomatedShippingSettings": true
      },
      "buyerInfo": {
        "buyerEmail": "ava@example.com"
      },
      "defaultShipFromLocationAddress": {
        "addressLine1": "string",
        "city": "string",
        "countryCode": "string",
        "name": "Ava Chen",
        "postalCode": "string",
        "stateOrRegion": "string"
      },
      "earliestDeliveryDate": "string",
      "earliestShipDate": "string",
      "fulfillmentChannel": "string",
      "hasRegulatedItems": true,
      "isAccessPointOrder": true,
      "isBusinessOrder": true,
      "isGlobalExpressEnabled": true,
      "isISPU": true,
      "isPremiumOrder": true,
      "isPrime": true,
      "isReplacementOrder": "string",
      "isSoldByAB": true,
      "lastUpdateDate": "string",
      "latestDeliveryDate": "string",
      "latestShipDate": "string",
      "marketplaceId": "string",
      "numberOfItemsShipped": 1,
      "numberOfItemsUnshipped": 1,
      "orderStatus": "string",
      "orderTotal": {
        "amount": "string",
        "currencyCode": "string"
      },
      "orderType": "string",
      "paymentMethod": "string",
      "paymentMethodDetails": [
        "string"
      ],
      "purchaseDate": "string",
      "salesChannel": "string",
      "shipmentServiceLevelCategory": "string",
      "shippingAddress": {
        "city": "string",
        "countryCode": "string",
        "postalCode": "string",
        "stateOrRegion": "string"
      },
      "shipServiceLevel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amazonOrderId` | string |  |
| `automatedShippingSettings.automatedCarrier` | string |  |
| `automatedShippingSettings.automatedCarrierName` | string |  |
| `automatedShippingSettings.automatedShipMethod` | string |  |
| `automatedShippingSettings.automatedShipMethodName` | string |  |
| `automatedShippingSettings.hasAutomatedShippingSettings` | boolean |  |
| `buyerInfo.buyerEmail` | string |  |
| `defaultShipFromLocationAddress.addressLine1` | string |  |
| `defaultShipFromLocationAddress.city` | string |  |
| `defaultShipFromLocationAddress.countryCode` | string |  |
| `defaultShipFromLocationAddress.name` | string |  |
| `defaultShipFromLocationAddress.postalCode` | string |  |
| `defaultShipFromLocationAddress.stateOrRegion` | string |  |
| `earliestDeliveryDate` | string |  |
| `earliestShipDate` | string |  |
| `fulfillmentChannel` | string |  |
| `hasRegulatedItems` | boolean |  |
| `isAccessPointOrder` | boolean |  |
| `isBusinessOrder` | boolean |  |
| `isGlobalExpressEnabled` | boolean |  |
| `isISPU` | boolean |  |
| `isPremiumOrder` | boolean |  |
| `isPrime` | boolean |  |
| `isReplacementOrder` | string |  |
| `isSoldByAB` | boolean |  |
| `lastUpdateDate` | string |  |
| `latestDeliveryDate` | string |  |
| `latestShipDate` | string |  |
| `marketplaceId` | string |  |
| `numberOfItemsShipped` | number |  |
| `numberOfItemsUnshipped` | number |  |
| `orderStatus` | string |  |
| `orderTotal.amount` | string |  |
| `orderTotal.currencyCode` | string |  |
| `orderType` | string |  |
| `paymentMethod` | string |  |
| `paymentMethodDetails[]` | string |  |
| `purchaseDate` | string |  |
| `salesChannel` | string |  |
| `shipmentServiceLevelCategory` | string |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.countryCode` | string |  |
| `shippingAddress.postalCode` | string |  |
| `shippingAddress.stateOrRegion` | string |  |
| `shipServiceLevel` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET sellers/v1/marketplaceParticipations` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-marketplace-participations.md) for the provider-specific parameters and requirements.

