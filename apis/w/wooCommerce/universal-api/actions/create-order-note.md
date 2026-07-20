# WooCommerce: Create Order Note

Creates an order note in WooCommerce.

```
PUT https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-order-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-order-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-order-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | list<number> | yes | Unique numeric ID of the order to update. |
| `note` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billing": {},
      "cartHash": "string",
      "cartTax": "string",
      "couponLines": [
        {}
      ],
      "createdVia": "string",
      "currency": "string",
      "currencySymbol": "string",
      "customerId": 1,
      "customerIpAddress": "string",
      "customerNote": "string",
      "customerUserAgent": "string",
      "dateCompleted": "2026-05-07T12:00:00.000Z",
      "dateCompletedGmt": "2026-05-07T12:00:00.000Z",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateCreatedGmt": "2026-05-07T12:00:00.000Z",
      "dateModified": "2026-05-07T12:00:00.000Z",
      "dateModifiedGmt": "2026-05-07T12:00:00.000Z",
      "datePaid": "2026-05-07T12:00:00.000Z",
      "datePaidGmt": "2026-05-07T12:00:00.000Z",
      "discountTax": "string",
      "discountTotal": "string",
      "feeLines": [
        {}
      ],
      "id": 1,
      "isEditable": true,
      "lineItems": [
        {}
      ],
      "metaData": [
        {}
      ],
      "needsPayment": true,
      "needsProcessing": true,
      "number": "string",
      "orderKey": "string",
      "parentId": 1,
      "paymentMethod": "string",
      "paymentMethodTitle": "string",
      "paymentUrl": "https://example.com",
      "pricesIncludeTax": true,
      "refunds": [
        {}
      ],
      "shipping": {},
      "shippingLines": [
        {}
      ],
      "shippingTax": "string",
      "shippingTotal": "string",
      "status": "string",
      "taxLines": [
        {}
      ],
      "total": "string",
      "totalTax": "string",
      "transactionId": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing` | object |  |
| `cartHash` | string |  |
| `cartTax` | string |  |
| `couponLines` | array<object> |  |
| `createdVia` | string |  |
| `currency` | string |  |
| `currencySymbol` | string |  |
| `customerId` | number |  |
| `customerIpAddress` | string |  |
| `customerNote` | string |  |
| `customerUserAgent` | string |  |
| `dateCompleted` | date |  |
| `dateCompletedGmt` | date |  |
| `dateCreated` | date |  |
| `dateCreatedGmt` | date |  |
| `dateModified` | date |  |
| `dateModifiedGmt` | date |  |
| `datePaid` | date |  |
| `datePaidGmt` | date |  |
| `discountTax` | string |  |
| `discountTotal` | string |  |
| `feeLines` | array<object> |  |
| `id` | number |  |
| `isEditable` | boolean |  |
| `lineItems` | array<object> |  |
| `metaData` | array<object> |  |
| `needsPayment` | boolean |  |
| `needsProcessing` | boolean |  |
| `number` | string |  |
| `orderKey` | string |  |
| `parentId` | number |  |
| `paymentMethod` | string |  |
| `paymentMethodTitle` | string |  |
| `paymentUrl` | string |  |
| `pricesIncludeTax` | boolean |  |
| `refunds` | array<object> |  |
| `shipping` | object |  |
| `shippingLines` | array<object> |  |
| `shippingTax` | string |  |
| `shippingTotal` | string |  |
| `status` | string |  |
| `taxLines` | array<object> |  |
| `total` | string |  |
| `totalTax` | string |  |
| `transactionId` | string |  |
| `version` | string |  |

## Native endpoint

Through the native WooCommerce API, this operation is `POST /orders/:id/notes` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order-note.md) for the provider-specific parameters and requirements.

