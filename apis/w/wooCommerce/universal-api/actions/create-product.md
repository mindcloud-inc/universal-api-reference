# WooCommerce: Create Product

Creates a new product in WooCommerce.

```
POST https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/create-product', {
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
| `name` | string | no | Product name. |
| `type` | list<string> | no | Product type such as simple, grouped, external, or variable. One of: `external`, `grouped`, `simple`, `variable`. |
| `regularPrice` | string | no | Regular product price as a string amount. |
| `salePrice` | string | no | Sale price as a string amount. |
| `sku` | string | no |  |
| `description` | string | no | Full product description in text or HTML. |
| `shortDescription` | string | no | Short product description in text or HTML. |
| `virtual` | boolean | no |  |
| `downloadable` | boolean | no |  |
| `manageStock` | boolean | no |  |
| `stockQuantity` | number | no |  |
| `status` | list<string> | no | Catalog status such as draft, pending, private, or publish. One of: `draft`, `pending`, `private`, `publish`. |
| `categories[]` | array<object> | no |  |
| `categories[].id` | number | no |  |
| `images[]` | array<object> | no |  |
| `images[].id` | number | no |  |
| `images[].src` | string | no |  |
| `images[].name` | string | no |  |
| `images[].alt` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "averageRating": "string",
      "catalogVisibility": "string",
      "categories": [
        {}
      ],
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateCreatedGmt": "2026-05-07T12:00:00.000Z",
      "dateModified": "2026-05-07T12:00:00.000Z",
      "dateModifiedGmt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dimensions": {},
      "downloadable": true,
      "featured": true,
      "hasOptions": true,
      "id": 1,
      "images": [
        {}
      ],
      "menuOrder": 1,
      "name": "Ava Chen",
      "onSale": true,
      "parentId": 1,
      "permalink": "https://example.com",
      "price": "string",
      "purchasable": true,
      "ratingCount": 1,
      "regularPrice": "string",
      "reviewsAllowed": true,
      "salePrice": "string",
      "shippingRequired": true,
      "shippingTaxable": true,
      "shortDescription": "string",
      "sku": "string",
      "slug": "string",
      "status": "string",
      "stockStatus": "string",
      "tags": [
        {}
      ],
      "totalSales": 1,
      "type": "string",
      "virtual": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageRating` | string |  |
| `catalogVisibility` | string |  |
| `categories` | array<object> |  |
| `dateCreated` | date |  |
| `dateCreatedGmt` | date |  |
| `dateModified` | date |  |
| `dateModifiedGmt` | date |  |
| `description` | string |  |
| `dimensions` | object |  |
| `downloadable` | boolean |  |
| `featured` | boolean |  |
| `hasOptions` | boolean |  |
| `id` | number |  |
| `images` | array<object> |  |
| `menuOrder` | number |  |
| `name` | string |  |
| `onSale` | boolean |  |
| `parentId` | number |  |
| `permalink` | string |  |
| `price` | string |  |
| `purchasable` | boolean |  |
| `ratingCount` | number |  |
| `regularPrice` | string |  |
| `reviewsAllowed` | boolean |  |
| `salePrice` | string |  |
| `shippingRequired` | boolean |  |
| `shippingTaxable` | boolean |  |
| `shortDescription` | string |  |
| `sku` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `stockStatus` | string |  |
| `tags` | array<object> |  |
| `totalSales` | number |  |
| `type` | string |  |
| `virtual` | boolean |  |

## Native endpoint

Through the native WooCommerce API, this operation is `POST /products` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

