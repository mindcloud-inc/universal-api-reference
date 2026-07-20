# SquareSpace: Create Product

Creates a product in Squarespace.

```
POST https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "storePageId": "string",
  "type": "GIFT_CARD"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "storePageId": "string",
    "type": "GIFT_CARD"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Product description. |
| `isVisible` | boolean | no | Whether product is visible on storefront. |
| `name` | string | yes | Product name. |
| `storePageId` | list<string> | yes | Target store page ID where the product is created. |
| `tags[]` | array<string> | no | Product tags. |
| `type` | list<string> | yes | Product type (for example PHYSICAL). One of: `GIFT_CARD`, `PHYSICAL`, `SERVICE`. |
| `variants[]` | array<object> | no | List of product variants. |
| `variants[].pricing.basePrice.currency` | string | no | Variant base price currency (ISO code). |
| `variants[].pricing.basePrice.value` | string | no | Variant base price amount. |
| `variants[].sku` | string | no | Variant SKU code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "string",
      "description": "string",
      "id": "string",
      "images": [
        {}
      ],
      "isVisible": true,
      "modifiedOn": "string",
      "name": "Ava Chen",
      "seoOptions": {},
      "storePageId": "string",
      "tags": [
        "string"
      ],
      "type": "string",
      "url": "https://example.com",
      "urlSlug": "https://example.com",
      "variantAttributes": [
        "string"
      ],
      "variants": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | string |  |
| `description` | string |  |
| `id` | string |  |
| `images` | array<object> |  |
| `isVisible` | boolean |  |
| `modifiedOn` | string |  |
| `name` | string |  |
| `seoOptions` | object |  |
| `storePageId` | string |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `url` | string |  |
| `urlSlug` | string |  |
| `variantAttributes` | array<string> |  |
| `variants` | array<object> |  |

## Native endpoint

Through the native SquareSpace API, this operation is `POST /v2/commerce/products` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

