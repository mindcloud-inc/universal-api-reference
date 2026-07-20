# SquareSpace: Get Order

Retrieves an order from Squarespace.

```
GET https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-order?${params}`, {
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
| `id` | list<string> | yes | Order ID to retrieve. |

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

Through the native SquareSpace API, this operation is `GET /1.0/commerce/orders/:id` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

