# SquareSpace: Create Order

Creates an order in Squarespace.

```
POST https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelName": "Ava Chen",
  "createdOn": "2026-05-07T12:00:00.000Z",
  "externalOrderReference": "string",
  "grandTotal.currency": "string",
  "grandTotal.value": "string",
  "idempotencyKey": "string",
  "lineItems[]": [
    {}
  ],
  "lineItems[].lineItemType": "CUSTOM",
  "lineItems[].quantity": 1,
  "lineItems[].unitPricePaid.currency": "string",
  "lineItems[].unitPricePaid.value": "string",
  "lineItems[].variantId": "string",
  "priceTaxInterpretation": "EXCLUSIVE",
  "subtotal.currency": "string",
  "subtotal.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelName": "Ava Chen",
    "createdOn": "2026-05-07T12:00:00.000Z",
    "externalOrderReference": "string",
    "grandTotal.currency": "string",
    "grandTotal.value": "string",
    "idempotencyKey": "string",
    "lineItems[]": [{}],
    "lineItems[].lineItemType": "CUSTOM",
    "lineItems[].quantity": 1,
    "lineItems[].unitPricePaid.currency": "string",
    "lineItems[].unitPricePaid.value": "string",
    "lineItems[].variantId": "string",
    "priceTaxInterpretation": "EXCLUSIVE",
    "subtotal.currency": "string",
    "subtotal.value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelName` | string | yes | Sales channel name for the order. |
| `createdOn` | date | yes | Order creation datetime in ISO 8601 UTC format. |
| `customerEmail` | string | no | Customer email address. |
| `externalOrderReference` | string | yes | External system order reference. |
| `grandTotal.currency` | string | yes | ISO 4217 currency code for order grand total. |
| `grandTotal.value` | string | yes | Monetary amount for order grand total. |
| `idempotencyKey` | string | yes | Unique idempotency key for safe create-order retries. |
| `lineItems[]` | array<object> | yes | Order line items. |
| `lineItems[].lineItemType` | list<string> | yes | Product type sold for each line item. One of: `CUSTOM`, `PHYSICAL_PRODUCT`. |
| `lineItems[].quantity` | number | yes | Quantity for line item. |
| `lineItems[].unitPricePaid.currency` | string | yes | ISO 4217 currency code for line item unit price. |
| `lineItems[].unitPricePaid.value` | string | yes | Monetary amount for line item unit price. |
| `lineItems[].variantId` | list<string> | yes | Variant ID for line item. |
| `priceTaxInterpretation` | list<string> | yes | Whether item prices include or exclude tax. One of: `EXCLUSIVE`, `INCLUSIVE`. |
| `subtotal.currency` | string | yes | ISO 4217 currency code for order subtotal. |
| `subtotal.value` | string | yes | Monetary amount for order subtotal. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAddress": {},
      "channel": "string",
      "channelName": "Ava Chen",
      "createdOn": "string",
      "customerEmail": "ava@example.com",
      "discountLines": [
        {}
      ],
      "discountTotal": {},
      "externalOrderReference": "string",
      "formSubmission": [
        {}
      ],
      "fulfilledOn": "string",
      "fulfillments": [
        {}
      ],
      "fulfillmentStatus": "string",
      "grandTotal": {},
      "id": "string",
      "internalNotes": [
        {}
      ],
      "lineItems": [
        {}
      ],
      "modifiedOn": "string",
      "orderNumber": "string",
      "priceTaxInterpretation": "string",
      "refundedTotal": {},
      "shippingAddress": {},
      "shippingLines": [
        {}
      ],
      "shippingTotal": {},
      "subtotal": {},
      "taxTotal": {},
      "testmode": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress` | object |  |
| `channel` | string |  |
| `channelName` | string |  |
| `createdOn` | string |  |
| `customerEmail` | string |  |
| `discountLines` | array<object> |  |
| `discountTotal` | object |  |
| `externalOrderReference` | string |  |
| `formSubmission` | array<object> |  |
| `fulfilledOn` | string |  |
| `fulfillments` | array<object> |  |
| `fulfillmentStatus` | string |  |
| `grandTotal` | object |  |
| `id` | string |  |
| `internalNotes` | array<object> |  |
| `lineItems` | array<object> |  |
| `modifiedOn` | string |  |
| `orderNumber` | string |  |
| `priceTaxInterpretation` | string |  |
| `refundedTotal` | object |  |
| `shippingAddress` | object |  |
| `shippingLines` | array<object> |  |
| `shippingTotal` | object |  |
| `subtotal` | object |  |
| `taxTotal` | object |  |
| `testmode` | boolean |  |

## Native endpoint

Through the native SquareSpace API, this operation is `POST /1.0/commerce/orders` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

