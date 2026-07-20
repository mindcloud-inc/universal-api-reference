# Starshipit: Get Order(s)



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/get-order-s
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/get-order-s?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/get-order-s?${params}`, {
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
| `orderId` | string | no | The unique numeric identifier for the order |
| `orderNumber` | string | no | The identifier of the order pulled from source e-Commerce platform |
| `status` | string | no |  |
| `filter` | string | no |  |
| `include` | string | no |  |
| `sortColumn` | string | no | Order field to sort by. |
| `sortDirection` | string | no |  |
| `pageNumber` | string | no |  |

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

Through the native Starshipit API, this operation is `GET /orders` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-s.md) for the provider-specific parameters and requirements.

