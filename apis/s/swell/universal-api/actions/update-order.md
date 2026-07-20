# Swell: Update Order



```
PUT https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Swell order ID. |
| `accountId` | string | no | The Swell account ID. |
| `items[]` | array<object> | yes | Order line items. |
| `billing` | object | no | Billing details. |
| `shipping` | object | no | Shipping details. |
| `couponCode` | string | no | A coupon code to apply. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "closed": true,
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "delivered": true,
      "discountTotal": 1,
      "giftcardTotal": 1,
      "grandTotal": 1,
      "guest": true,
      "hold": true,
      "id": "string",
      "itemDiscount": 1,
      "itemQuantity": 1,
      "itemQuantityCancelable": 1,
      "itemQuantityCanceled": 1,
      "itemQuantityCreditable": 1,
      "itemQuantityCredited": 1,
      "itemQuantityDeliverable": 1,
      "itemQuantityDelivered": 1,
      "itemQuantityInvoiceable": 1,
      "itemQuantityInvoiced": 1,
      "itemQuantityReturnable": 1,
      "itemQuantityReturned": 1,
      "itemQuantityShipmentDeliverable": 1,
      "items": [
        {
          "delivery": "string",
          "discountEach": 1,
          "discountTotal": 1,
          "id": "string",
          "price": 1,
          "priceTotal": 1,
          "productId": "string",
          "productName": "Ava Chen",
          "quantity": 1,
          "quantityCancelable": 1,
          "quantityCanceled": 1,
          "quantityCreditable": 1,
          "quantityDeliverable": 1,
          "quantityDelivered": 1,
          "quantityInvoiceable": 1,
          "quantityShipmentDeliverable": 1,
          "quantityTotal": 1,
          "shipmentWeight": 1,
          "taxEach": 1,
          "taxTotal": 1
        }
      ],
      "itemShipmentWeight": 1,
      "itemTax": 1,
      "number": "string",
      "paid": true,
      "paymentBalance": 1,
      "paymentTotal": 1,
      "refunded": true,
      "refundTotal": 1,
      "returnItemTax": 1,
      "returnItemTaxIncluded": 1,
      "returnItemTotal": 1,
      "returnTotal": 1,
      "shipmentDelivery": true,
      "shipmentPrice": 1,
      "shipmentTaxIncludedTotal": 1,
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
| `accountId` | string |  |
| `closed` | boolean |  |
| `currency` | string |  |
| `dateCreated` | date |  |
| `delivered` | boolean |  |
| `discountTotal` | number |  |
| `giftcardTotal` | number |  |
| `grandTotal` | number |  |
| `guest` | boolean |  |
| `hold` | boolean |  |
| `id` | string |  |
| `itemDiscount` | number |  |
| `itemQuantity` | number |  |
| `itemQuantityCancelable` | number |  |
| `itemQuantityCanceled` | number |  |
| `itemQuantityCreditable` | number |  |
| `itemQuantityCredited` | number |  |
| `itemQuantityDeliverable` | number |  |
| `itemQuantityDelivered` | number |  |
| `itemQuantityInvoiceable` | number |  |
| `itemQuantityInvoiced` | number |  |
| `itemQuantityReturnable` | number |  |
| `itemQuantityReturned` | number |  |
| `itemQuantityShipmentDeliverable` | number |  |
| `items[].delivery` | string |  |
| `items[].discountEach` | number |  |
| `items[].discountTotal` | number |  |
| `items[].id` | string |  |
| `items[].price` | number |  |
| `items[].priceTotal` | number |  |
| `items[].productId` | string |  |
| `items[].productName` | string |  |
| `items[].quantity` | number |  |
| `items[].quantityCancelable` | number |  |
| `items[].quantityCanceled` | number |  |
| `items[].quantityCreditable` | number |  |
| `items[].quantityDeliverable` | number |  |
| `items[].quantityDelivered` | number |  |
| `items[].quantityInvoiceable` | number |  |
| `items[].quantityShipmentDeliverable` | number |  |
| `items[].quantityTotal` | number |  |
| `items[].shipmentWeight` | number |  |
| `items[].taxEach` | number |  |
| `items[].taxTotal` | number |  |
| `itemShipmentWeight` | number |  |
| `itemTax` | number |  |
| `number` | string |  |
| `paid` | boolean |  |
| `paymentBalance` | number |  |
| `paymentTotal` | number |  |
| `refunded` | boolean |  |
| `refundTotal` | number |  |
| `returnItemTax` | number |  |
| `returnItemTaxIncluded` | number |  |
| `returnItemTotal` | number |  |
| `returnTotal` | number |  |
| `shipmentDelivery` | boolean |  |
| `shipmentPrice` | number |  |
| `shipmentTaxIncludedTotal` | number |  |
| `shipmentTotal` | number |  |
| `status` | string |  |
| `subTotal` | number |  |
| `taxIncludedTotal` | number |  |
| `taxTotal` | number |  |

## Native endpoint

Through the native Swell API, this operation is `PUT /orders/:id` (base URL `https://api.swell.store`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.

