# Starshipit: Clone Shipment



```
POST https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/clone-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/clone-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/clone-shipment', {
  method: 'POST',
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
| `orderId` | number | no |  |
| `toReturnShipment` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order": {
        "addInsurance": true,
        "addressValidation": "string",
        "archived": true,
        "carrier": "string",
        "carrierName": "Ava Chen",
        "carrierServiceCode": "string",
        "createReturn": true,
        "currency": "string",
        "dangerousGoods": true,
        "declaredValue": 1,
        "destination": {
          "building": "string",
          "city": "string",
          "company": "string",
          "country": "string",
          "deliveryInstructions": "string",
          "email": "ava@example.com",
          "name": "Ava Chen",
          "phone": "string",
          "postCode": "string",
          "state": "string",
          "street": "string",
          "suburb": "string"
        },
        "dtp": true,
        "events": [
          {
            "category": "string",
            "description": "string",
            "method": "string",
            "time": "2026-05-07T12:00:00.000Z"
          }
        ],
        "exportType": "string",
        "insuranceValue": 1,
        "items": [
          {
            "countryOfOrigin": "string",
            "description": "string",
            "itemId": 1,
            "quantity": 1,
            "quantityToShip": 1,
            "sku": "string",
            "value": 1,
            "weight": 1
          }
        ],
        "manifested": true,
        "manifestNumber": 1,
        "metadatas": [
          {
            "metafieldKey": "string",
            "value": "string"
          }
        ],
        "orderDate": "2026-05-07T12:00:00.000Z",
        "orderId": 1,
        "orderNumber": "string",
        "packages": [
          {
            "carrierServiceCode": "string",
            "contents": "string",
            "deliveryStatus": "string",
            "height": 1,
            "length": 1,
            "name": "Ava Chen",
            "packageId": 1,
            "packagingType": "string",
            "shipmentType": "string",
            "trackingNumber": "string",
            "trackingUrl": "https://example.com",
            "weight": 1,
            "width": 1
          }
        ],
        "platform": "string",
        "plt": true,
        "reference": "string",
        "senderDetails": {
          "building": "string",
          "city": "string",
          "company": "string",
          "country": "string",
          "email": "ava@example.com",
          "name": "Ava Chen",
          "phone": "string",
          "postCode": "string",
          "state": "string",
          "street": "string",
          "suburb": "string"
        },
        "shippingMethod": "string",
        "signatureRequired": true,
        "status": "string",
        "type": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `order` | object |  |
| `order.addInsurance` | boolean |  |
| `order.addressValidation` | string |  |
| `order.archived` | boolean |  |
| `order.carrier` | string |  |
| `order.carrierName` | string |  |
| `order.carrierServiceCode` | string |  |
| `order.createReturn` | boolean |  |
| `order.currency` | string |  |
| `order.dangerousGoods` | boolean |  |
| `order.declaredValue` | number |  |
| `order.destination` | object |  |
| `order.destination.building` | string |  |
| `order.destination.city` | string |  |
| `order.destination.company` | string |  |
| `order.destination.country` | string |  |
| `order.destination.deliveryInstructions` | string |  |
| `order.destination.email` | string |  |
| `order.destination.name` | string |  |
| `order.destination.phone` | string |  |
| `order.destination.postCode` | string |  |
| `order.destination.state` | string |  |
| `order.destination.street` | string |  |
| `order.destination.suburb` | string |  |
| `order.dtp` | boolean |  |
| `order.events` | array<object> |  |
| `order.events[].category` | string |  |
| `order.events[].description` | string |  |
| `order.events[].method` | string |  |
| `order.events[].time` | date |  |
| `order.exportType` | string |  |
| `order.insuranceValue` | number |  |
| `order.items` | array<object> |  |
| `order.items[].countryOfOrigin` | string |  |
| `order.items[].description` | string |  |
| `order.items[].itemId` | number |  |
| `order.items[].quantity` | number |  |
| `order.items[].quantityToShip` | number |  |
| `order.items[].sku` | string |  |
| `order.items[].value` | number |  |
| `order.items[].weight` | number |  |
| `order.manifested` | boolean |  |
| `order.manifestNumber` | number |  |
| `order.metadatas` | array<object> |  |
| `order.metadatas[].metafieldKey` | string |  |
| `order.metadatas[].value` | string |  |
| `order.orderDate` | date |  |
| `order.orderId` | number |  |
| `order.orderNumber` | string |  |
| `order.packages` | array<object> |  |
| `order.packages[].carrierServiceCode` | string |  |
| `order.packages[].contents` | string |  |
| `order.packages[].deliveryStatus` | string |  |
| `order.packages[].height` | number |  |
| `order.packages[].length` | number |  |
| `order.packages[].name` | string |  |
| `order.packages[].packageId` | number |  |
| `order.packages[].packagingType` | string |  |
| `order.packages[].shipmentType` | string |  |
| `order.packages[].trackingNumber` | string |  |
| `order.packages[].trackingUrl` | string |  |
| `order.packages[].weight` | number |  |
| `order.packages[].width` | number |  |
| `order.platform` | string |  |
| `order.plt` | boolean |  |
| `order.reference` | string |  |
| `order.senderDetails` | object |  |
| `order.senderDetails.building` | string |  |
| `order.senderDetails.city` | string |  |
| `order.senderDetails.company` | string |  |
| `order.senderDetails.country` | string |  |
| `order.senderDetails.email` | string |  |
| `order.senderDetails.name` | string |  |
| `order.senderDetails.phone` | string |  |
| `order.senderDetails.postCode` | string |  |
| `order.senderDetails.state` | string |  |
| `order.senderDetails.street` | string |  |
| `order.senderDetails.suburb` | string |  |
| `order.shippingMethod` | string |  |
| `order.signatureRequired` | boolean |  |
| `order.status` | string |  |
| `order.type` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `POST /orders/shipment/clone` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clone-shipment.md) for the provider-specific parameters and requirements.

