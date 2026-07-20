# Starshipit: Update Order



```
PUT https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/update-order', {
  method: 'PUT',
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
| `order.orderId` | number | no |  |
| `order.orderDate` | date | no |  |
| `order.orderNumber` | string | no |  |
| `order.reference` | string | no |  |
| `order.carrier` | string | no |  |
| `order.carrierServiceCode` | string | no |  |
| `order.shippingMethod` | string | no |  |
| `order.signatureRequired` | boolean | no |  |
| `order.destination.name` | string | no |  |
| `order.destination.phone` | string | no |  |
| `order.destination.street` | string | no |  |
| `order.destination.suburb` | string | no |  |
| `order.destination.state` | string | no |  |
| `order.destination.postCode` | string | no |  |
| `order.destination.country` | string | no |  |
| `order.destination.deliveryInstructions` | string | no |  |
| `order.items[]` | array<object> | no |  |
| `order.packages[]` | array<object> | no |  |

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
        "dangerousGoods": true,
        "declaredValue": 1,
        "destination": {
          "country": "string",
          "deliveryInstructions": "string",
          "name": "Ava Chen",
          "phone": "string",
          "postCode": "string",
          "state": "string",
          "street": "string",
          "suburb": "string"
        },
        "dtp": true,
        "insuranceValue": 1,
        "items": [
          {
            "description": "string",
            "itemId": 1,
            "quantity": 1,
            "quantityToShip": 1,
            "sku": "string",
            "value": 1,
            "weight": 1
          }
        ],
        "manifestNumber": 1,
        "orderDate": "2026-05-07T12:00:00.000Z",
        "orderId": 1,
        "orderNumber": "string",
        "packages": [
          {
            "height": 1,
            "length": 1,
            "packageId": 1,
            "weight": 1,
            "width": 1
          }
        ],
        "platform": "string",
        "plt": true,
        "reference": "string",
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
| `order.dangerousGoods` | boolean |  |
| `order.declaredValue` | number |  |
| `order.destination` | object |  |
| `order.destination.country` | string |  |
| `order.destination.deliveryInstructions` | string |  |
| `order.destination.name` | string |  |
| `order.destination.phone` | string |  |
| `order.destination.postCode` | string |  |
| `order.destination.state` | string |  |
| `order.destination.street` | string |  |
| `order.destination.suburb` | string |  |
| `order.dtp` | boolean |  |
| `order.insuranceValue` | number |  |
| `order.items` | array<object> |  |
| `order.items[].description` | string |  |
| `order.items[].itemId` | number |  |
| `order.items[].quantity` | number |  |
| `order.items[].quantityToShip` | number |  |
| `order.items[].sku` | string |  |
| `order.items[].value` | number |  |
| `order.items[].weight` | number |  |
| `order.manifestNumber` | number |  |
| `order.orderDate` | date |  |
| `order.orderId` | number |  |
| `order.orderNumber` | string |  |
| `order.packages` | array<object> |  |
| `order.packages[].height` | number |  |
| `order.packages[].length` | number |  |
| `order.packages[].packageId` | number |  |
| `order.packages[].weight` | number |  |
| `order.packages[].width` | number |  |
| `order.platform` | string |  |
| `order.plt` | boolean |  |
| `order.reference` | string |  |
| `order.shippingMethod` | string |  |
| `order.signatureRequired` | boolean |  |
| `order.status` | string |  |
| `order.type` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `PUT /orders` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.

