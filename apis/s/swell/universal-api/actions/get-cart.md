# Swell: Get Cart



```
GET https://connect.mindcloud.co/v1/universal/swell/latest/actions/get-cart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swell/latest/actions/get-cart?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swell/latest/actions/get-cart?${params}`, {
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
| `id` | string | yes | The Swell cart ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abandonedNotifications": 1,
      "active": true,
      "authTotal": 1,
      "captureTotal": 1,
      "checkoutId": "string",
      "checkoutUrl": "https://example.com",
      "currency": "string",
      "dateAbandoned": "2026-05-07T12:00:00.000Z",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateLastAccessed": "2026-05-07T12:00:00.000Z",
      "discountTotal": 1,
      "giftcardTotal": 1,
      "grandTotal": 1,
      "guest": true,
      "id": "string",
      "itemDiscount": 1,
      "itemQuantity": 1,
      "items": [
        {
          "delivery": "string",
          "discountEach": 1,
          "discountTotal": 1,
          "id": "string",
          "origPrice": 1,
          "price": 1,
          "priceTotal": 1,
          "productId": "string",
          "productName": "Ava Chen",
          "quantity": 1,
          "shipmentWeight": 1,
          "taxEach": 1,
          "taxTotal": 1
        }
      ],
      "itemShipmentWeight": 1,
      "itemTax": 1,
      "number": "string",
      "shipmentDelivery": true,
      "shipmentPrice": 1,
      "shipmentTotal": 1,
      "status": "string",
      "subTotal": 1,
      "taxIncludedTotal": 1,
      "taxTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abandonedNotifications` | number |  |
| `active` | boolean |  |
| `authTotal` | number |  |
| `captureTotal` | number |  |
| `checkoutId` | string |  |
| `checkoutUrl` | string |  |
| `currency` | string |  |
| `dateAbandoned` | date |  |
| `dateCreated` | date |  |
| `dateLastAccessed` | date |  |
| `discountTotal` | number |  |
| `giftcardTotal` | number |  |
| `grandTotal` | number |  |
| `guest` | boolean |  |
| `id` | string |  |
| `itemDiscount` | number |  |
| `itemQuantity` | number |  |
| `items[].delivery` | string |  |
| `items[].discountEach` | number |  |
| `items[].discountTotal` | number |  |
| `items[].id` | string |  |
| `items[].origPrice` | number |  |
| `items[].price` | number |  |
| `items[].priceTotal` | number |  |
| `items[].productId` | string |  |
| `items[].productName` | string |  |
| `items[].quantity` | number |  |
| `items[].shipmentWeight` | number |  |
| `items[].taxEach` | number |  |
| `items[].taxTotal` | number |  |
| `itemShipmentWeight` | number |  |
| `itemTax` | number |  |
| `number` | string |  |
| `shipmentDelivery` | boolean |  |
| `shipmentPrice` | number |  |
| `shipmentTotal` | number |  |
| `status` | string |  |
| `subTotal` | number |  |
| `taxIncludedTotal` | number |  |
| `taxTotal` | number |  |

## Native endpoint

Through the native Swell API, this operation is `GET /carts/:id` (base URL `https://api.swell.store`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cart.md) for the provider-specific parameters and requirements.

