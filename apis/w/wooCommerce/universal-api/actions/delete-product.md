# WooCommerce: Delete Product

Deletes an existing product from WooCommerce.

```
DELETE https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/delete-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/delete-product?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/delete-product?${params}`, {
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
| `force` | boolean | no | Whether to permanently delete the product. Defaults to false in WooCommerce. |
| `id` | list<number> | yes | Unique numeric ID of the product to delete. |

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

Through the native WooCommerce API, this operation is `DELETE /products/:id` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-product.md) for the provider-specific parameters and requirements.

