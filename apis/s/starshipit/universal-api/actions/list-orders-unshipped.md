# Starshipit: List Orders (Unshipped)



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-unshipped
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-unshipped?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-unshipped?${params}`, {
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
| `sinceOrderDate` | date | no | (optional) Show orders created after date in UTC (date-time in RFC3339 format) |
| `sinceLastUpdated` | date | no | (optional) Show orders recently updated after date in UTC (date-time in RFC3339 format) |
| `idsOnly` | string | no | (optional) Show all unshipped order_ids only |
| `limit` | string | no | (optional) Amount of results (default: 50) (maximum: 250) |
| `page` | string | no | (optional) Page to show (default: 1) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orders": [
        {
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
            "taxNumbers": [
              "string"
            ]
          },
          "dtp": true,
          "insuranceValue": 1,
          "items": [
            {
              "countryOfOrigin": "string",
              "description": "string",
              "height": 1,
              "itemId": 1,
              "length": 1,
              "quantity": 1,
              "quantityToShip": 1,
              "sku": "string",
              "stockOnHand": 1,
              "value": 1,
              "weight": 1,
              "width": 1
            }
          ],
          "manifestNumber": 1,
          "metadatas": [
            {
              "metafieldKey": "string",
              "required": true,
              "value": "string"
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
              "packagingType": "string",
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
            "suburb": "string",
            "taxNumbers": [
              "string"
            ]
          },
          "signatureRequired": true,
          "status": "string",
          "type": "string"
        }
      ],
      "success": true,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orders` | array<object> |  |
| `orders[].addInsurance` | boolean |  |
| `orders[].addressValidation` | string |  |
| `orders[].archived` | boolean |  |
| `orders[].carrier` | string |  |
| `orders[].carrierName` | string |  |
| `orders[].carrierServiceCode` | string |  |
| `orders[].createReturn` | boolean |  |
| `orders[].currency` | string |  |
| `orders[].dangerousGoods` | boolean |  |
| `orders[].declaredValue` | number |  |
| `orders[].destination` | object |  |
| `orders[].destination.building` | string |  |
| `orders[].destination.city` | string |  |
| `orders[].destination.company` | string |  |
| `orders[].destination.country` | string |  |
| `orders[].destination.deliveryInstructions` | string |  |
| `orders[].destination.email` | string |  |
| `orders[].destination.name` | string |  |
| `orders[].destination.phone` | string |  |
| `orders[].destination.postCode` | string |  |
| `orders[].destination.state` | string |  |
| `orders[].destination.street` | string |  |
| `orders[].destination.taxNumbers` | array<string> |  |
| `orders[].dtp` | boolean |  |
| `orders[].insuranceValue` | number |  |
| `orders[].items` | array<object> |  |
| `orders[].items[].countryOfOrigin` | string |  |
| `orders[].items[].description` | string |  |
| `orders[].items[].height` | number |  |
| `orders[].items[].itemId` | number |  |
| `orders[].items[].length` | number |  |
| `orders[].items[].quantity` | number |  |
| `orders[].items[].quantityToShip` | number |  |
| `orders[].items[].sku` | string |  |
| `orders[].items[].stockOnHand` | number |  |
| `orders[].items[].value` | number |  |
| `orders[].items[].weight` | number |  |
| `orders[].items[].width` | number |  |
| `orders[].manifestNumber` | number |  |
| `orders[].metadatas` | array<object> |  |
| `orders[].metadatas[].metafieldKey` | string |  |
| `orders[].metadatas[].required` | boolean |  |
| `orders[].metadatas[].value` | string |  |
| `orders[].orderDate` | date |  |
| `orders[].orderId` | number |  |
| `orders[].orderNumber` | string |  |
| `orders[].packages` | array<object> |  |
| `orders[].packages[].height` | number |  |
| `orders[].packages[].length` | number |  |
| `orders[].packages[].packageId` | number |  |
| `orders[].packages[].packagingType` | string |  |
| `orders[].packages[].weight` | number |  |
| `orders[].packages[].width` | number |  |
| `orders[].platform` | string |  |
| `orders[].plt` | boolean |  |
| `orders[].reference` | string |  |
| `orders[].senderDetails` | object |  |
| `orders[].senderDetails.building` | string |  |
| `orders[].senderDetails.city` | string |  |
| `orders[].senderDetails.company` | string |  |
| `orders[].senderDetails.country` | string |  |
| `orders[].senderDetails.email` | string |  |
| `orders[].senderDetails.name` | string |  |
| `orders[].senderDetails.phone` | string |  |
| `orders[].senderDetails.postCode` | string |  |
| `orders[].senderDetails.state` | string |  |
| `orders[].senderDetails.street` | string |  |
| `orders[].senderDetails.suburb` | string |  |
| `orders[].senderDetails.taxNumbers` | array<string> |  |
| `orders[].signatureRequired` | boolean |  |
| `orders[].status` | string |  |
| `orders[].type` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Starshipit API, this operation is `GET /orders/unshipped` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders-unshipped.md) for the provider-specific parameters and requirements.

