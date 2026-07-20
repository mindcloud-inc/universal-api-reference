# Starshipit: Create Orders



```
POST https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/create-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/create-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/create-orders', {
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
| `orders[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orders": [
        {
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
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orders` | array<object> |  |
| `orders[].carrier` | string |  |
| `orders[].carrierName` | string |  |
| `orders[].carrierServiceCode` | string |  |
| `orders[].dangerousGoods` | boolean |  |
| `orders[].declaredValue` | number |  |
| `orders[].destination` | object |  |
| `orders[].destination.country` | string |  |
| `orders[].destination.deliveryInstructions` | string |  |
| `orders[].destination.name` | string |  |
| `orders[].destination.phone` | string |  |
| `orders[].destination.postCode` | string |  |
| `orders[].destination.state` | string |  |
| `orders[].destination.street` | string |  |
| `orders[].destination.suburb` | string |  |
| `orders[].items` | array<object> |  |
| `orders[].items[].description` | string |  |
| `orders[].items[].itemId` | number |  |
| `orders[].items[].quantity` | number |  |
| `orders[].items[].quantityToShip` | number |  |
| `orders[].items[].sku` | string |  |
| `orders[].items[].value` | number |  |
| `orders[].items[].weight` | number |  |
| `orders[].orderDate` | date |  |
| `orders[].orderId` | number |  |
| `orders[].orderNumber` | string |  |
| `orders[].packages` | array<object> |  |
| `orders[].packages[].height` | number |  |
| `orders[].packages[].length` | number |  |
| `orders[].packages[].packageId` | number |  |
| `orders[].packages[].weight` | number |  |
| `orders[].packages[].width` | number |  |
| `orders[].reference` | string |  |
| `orders[].shippingMethod` | string |  |
| `orders[].signatureRequired` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `POST /orders/import` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-orders.md) for the provider-specific parameters and requirements.

