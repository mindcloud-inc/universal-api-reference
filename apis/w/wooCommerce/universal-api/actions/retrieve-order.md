# WooCommerce: Retrieve Order

Retrieves an order from WooCommerce.

```
GET https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/retrieve-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/retrieve-order?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/retrieve-order?${params}`, {
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
| `id` | list<number> | yes | Unique numeric ID of the order to retrieve. |

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

Through the native WooCommerce API, this operation is `GET /orders/:id` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order.md) for the provider-specific parameters and requirements.

