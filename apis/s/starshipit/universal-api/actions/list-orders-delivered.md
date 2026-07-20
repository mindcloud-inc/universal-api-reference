# Starshipit: List Orders (Delivered)



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-delivered
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-delivered?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-orders-delivered?${params}`, {
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
| `orderRef` | string | no |  |

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
            "suburb": "string",
            "taxNumbers": [
              "string"
            ]
          },
          "dtp": true,
          "exportType": "string",
          "hasCommercialInvoice": true,
          "insuranceValue": 1,
          "isFullyPacked": true,
          "manifested": true,
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
              "barcode": "string",
              "carrierServiceCode": "string",
              "carrierServiceName": "Ava Chen",
              "deliveryStatus": "string",
              "height": 1,
              "labelCreatedDate": "2026-05-07T12:00:00.000Z",
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
          "type": "string",
          "writebackDetails": "string",
          "writebackStatus": "string"
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
| `orders[].destination.suburb` | string |  |
| `orders[].destination.taxNumbers` | array<string> |  |
| `orders[].dtp` | boolean |  |
| `orders[].exportType` | string |  |
| `orders[].hasCommercialInvoice` | boolean |  |
| `orders[].insuranceValue` | number |  |
| `orders[].isFullyPacked` | boolean |  |
| `orders[].manifested` | boolean |  |
| `orders[].manifestNumber` | number |  |
| `orders[].metadatas` | array<object> |  |
| `orders[].metadatas[].metafieldKey` | string |  |
| `orders[].metadatas[].required` | boolean |  |
| `orders[].metadatas[].value` | string |  |
| `orders[].orderDate` | date |  |
| `orders[].orderId` | number |  |
| `orders[].orderNumber` | string |  |
| `orders[].packages` | array<object> |  |
| `orders[].packages[].barcode` | string |  |
| `orders[].packages[].carrierServiceCode` | string |  |
| `orders[].packages[].carrierServiceName` | string |  |
| `orders[].packages[].deliveryStatus` | string |  |
| `orders[].packages[].height` | number |  |
| `orders[].packages[].labelCreatedDate` | date |  |
| `orders[].packages[].length` | number |  |
| `orders[].packages[].name` | string |  |
| `orders[].packages[].packageId` | number |  |
| `orders[].packages[].packagingType` | string |  |
| `orders[].packages[].shipmentType` | string |  |
| `orders[].packages[].trackingNumber` | string |  |
| `orders[].packages[].trackingUrl` | string |  |
| `orders[].packages[].weight` | number |  |
| `orders[].packages[].width` | number |  |
| `orders[].platform` | string |  |
| `orders[].plt` | boolean |  |
| `orders[].reference` | string |  |
| `orders[].senderDetails` | object |  |
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
| `orders[].writebackDetails` | string |  |
| `orders[].writebackStatus` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `GET /orders/delivered` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders-delivered.md) for the provider-specific parameters and requirements.

