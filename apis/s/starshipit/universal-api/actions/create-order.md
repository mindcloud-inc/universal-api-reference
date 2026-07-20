# Starshipit: Create Order



```
POST https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/create-order', {
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
| `order.orderDate` | date | no |  |
| `order.orderNumber` | string | no |  |
| `order.reference` | string | no |  |
| `order.carrier` | string | no |  |
| `order.carrierName` | string | no |  |
| `order.shippingMethod` | string | no |  |
| `order.signatureRequired` | boolean | no |  |
| `order.returnOrder` | boolean | no |  |
| `order.destination.name` | string | no |  |
| `order.destination.phone` | string | no |  |
| `order.destination.street` | string | no |  |
| `order.destination.suburb` | string | no |  |
| `order.destination.state` | string | no |  |
| `order.destination.postCode` | string | no |  |
| `order.destination.country` | string | no |  |
| `order.destination.deliveryInstructions` | string | no |  |
| `order.items[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order": {
        "carrier": "string",
        "carrierName": "Ava Chen",
        "carrierServiceCode": "string",
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
        "reference": "string",
        "shippingMethod": "string",
        "signatureRequired": true
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
| `order.carrier` | string |  |
| `order.carrierName` | string |  |
| `order.carrierServiceCode` | string |  |
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
| `order.items` | array<object> |  |
| `order.items[].description` | string |  |
| `order.items[].itemId` | number |  |
| `order.items[].quantity` | number |  |
| `order.items[].quantityToShip` | number |  |
| `order.items[].sku` | string |  |
| `order.items[].value` | number |  |
| `order.items[].weight` | number |  |
| `order.orderDate` | date |  |
| `order.orderId` | number |  |
| `order.orderNumber` | string |  |
| `order.packages` | array<object> |  |
| `order.packages[].height` | number |  |
| `order.packages[].length` | number |  |
| `order.packages[].packageId` | number |  |
| `order.packages[].weight` | number |  |
| `order.packages[].width` | number |  |
| `order.reference` | string |  |
| `order.shippingMethod` | string |  |
| `order.signatureRequired` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `POST /orders` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

