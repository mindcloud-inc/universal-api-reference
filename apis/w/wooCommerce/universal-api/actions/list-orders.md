# WooCommerce: List Orders

Retrieves orders from WooCommerce.

```
GET https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/list-orders?${params}`, {
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
| `search` | string | no | Limit results to those matching a string. |
| `after` | string | no | Limit response to resources published after a given ISO8601 date. |
| `before` | string | no | Limit response to resources published before a given ISO8601 date. |
| `status` | list<string> | no | Limit result set to orders assigned a specific status. One of: `any`, `cancelled`, `completed`, `failed`, `on-hold`, `pending`, `processing`, `refunded`, `trash`. |
| `customerId` | list<number> | no | Limit result set to orders assigned to a specific customer. |
| `productId` | list<number> | no | Limit result set to orders assigned to a specific product. |
| `order` | string | no |  |
| `modified_after` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `meta_key` | string | no |  |
| `meta_value` | string | no |  |

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

Through the native WooCommerce API, this operation is `GET /orders` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

