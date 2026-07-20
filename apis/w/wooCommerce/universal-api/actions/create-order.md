# WooCommerce: Create Order

Creates a new order in WooCommerce.

```
POST https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-order', {
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
| `status` | list<string> | no | Order status such as pending, processing, completed, or cancelled. One of: `cancelled`, `completed`, `failed`, `on-hold`, `pending`, `processing`, `refunded`, `trash`. |
| `setPaid` | boolean | no | Whether the order should be marked paid immediately. |
| `customerId` | list<number> | no | Numeric ID of the existing customer for the order. |
| `paymentMethod` | string | no |  |
| `paymentMethodTitle` | string | no |  |
| `billing` | object | no |  |
| `billing.firstName` | string | no |  |
| `billing.lastName` | string | no |  |
| `billing.company` | string | no |  |
| `billing.address1` | string | no |  |
| `shipping.phone` | string | no |  |
| `billing.address2` | string | no |  |
| `billing.city` | string | no |  |
| `billing.state` | string | no |  |
| `billing.postcode` | string | no |  |
| `meta_data[]` | array | no |  |
| `billing.country` | string | no |  |
| `billing.email` | string | no |  |
| `billing.phone` | string | no |  |
| `shipping` | object | no |  |
| `shipping.firstName` | string | no |  |
| `shipping.lastName` | string | no |  |
| `shipping.company` | string | no |  |
| `shipping.address1` | string | no |  |
| `shipping.address2` | string | no |  |
| `shipping.city` | string | no |  |
| `shipping.state` | string | no |  |
| `shipping.postcode` | string | no |  |
| `lineItems[]` | array<object> | no |  |
| `shipping.country` | string | no |  |
| `lineItems[].productId` | number | no |  |
| `lineItems[].variationId` | number | no |  |
| `lineItems[].quantity` | number | no |  |
| `lineItems[].name` | string | no |  |
| `lineItems[].taxClass` | string | no |  |
| `lineItems[].subtotal` | string | no |  |
| `lineItems[].total` | string | no |  |
| `shippingLines[]` | array<object> | no |  |
| `shippingLines[].methodId` | string | no |  |
| `shippingLines[].methodTitle` | string | no |  |
| `currency` | string | no |  |
| `shippingLines[].total` | string | no |  |
| `customerNote` | string | no |  |
| `feeLines[]` | array<object> | no |  |
| `feeLines[].name` | string | no |  |
| `feeLines[].taxClass` | string | no |  |
| `feeLines[].taxStatus` | string | no |  |
| `couponLines[]` | array<object> | no |  |
| `feeLines[].total` | string | no |  |
| `couponLines[].code` | string | no |  |
| `couponLines[].discount` | string | no |  |

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

Through the native WooCommerce API, this operation is `POST /orders` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

