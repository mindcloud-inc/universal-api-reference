# WooCommerce: Duplicate Product

Creates a duplicate product in WooCommerce.

```
POST https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/duplicate-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WooCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/duplicate-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/duplicate-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | list<number> | yes | Unique numeric ID of the product to duplicate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": [
        {}
      ],
      "averageRating": "string",
      "backorders": "string",
      "catalogVisibility": "string",
      "categoryIds": [
        1
      ],
      "dateCreated": {},
      "dateModified": {},
      "defaultAttributes": [
        {}
      ],
      "description": "string",
      "downloadable": true,
      "downloadExpiry": 1,
      "downloadLimit": 1,
      "downloads": [
        {}
      ],
      "featured": true,
      "globalUniqueId": "string",
      "id": 1,
      "manageStock": true,
      "menuOrder": 1,
      "metaData": [
        {}
      ],
      "name": "Ava Chen",
      "parentId": 1,
      "postPassword": "string",
      "price": "string",
      "purchaseNote": "string",
      "regularPrice": "string",
      "reviewCount": 1,
      "reviewsAllowed": true,
      "salePrice": "string",
      "shippingClassId": 1,
      "shortDescription": "string",
      "sku": "string",
      "slug": "string",
      "soldIndividually": true,
      "status": "string",
      "stockStatus": "string",
      "taxClass": "string",
      "taxStatus": "string",
      "totalSales": 1,
      "virtual": true,
      "weight": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | array<object> |  |
| `averageRating` | string |  |
| `backorders` | string |  |
| `catalogVisibility` | string |  |
| `categoryIds` | array<number> |  |
| `dateCreated` | object |  |
| `dateModified` | object |  |
| `defaultAttributes` | array<object> |  |
| `description` | string |  |
| `downloadable` | boolean |  |
| `downloadExpiry` | number |  |
| `downloadLimit` | number |  |
| `downloads` | array<object> |  |
| `featured` | boolean |  |
| `globalUniqueId` | string |  |
| `id` | number |  |
| `manageStock` | boolean |  |
| `menuOrder` | number |  |
| `metaData` | array<object> |  |
| `name` | string |  |
| `parentId` | number |  |
| `postPassword` | string |  |
| `price` | string |  |
| `purchaseNote` | string |  |
| `regularPrice` | string |  |
| `reviewCount` | number |  |
| `reviewsAllowed` | boolean |  |
| `salePrice` | string |  |
| `shippingClassId` | number |  |
| `shortDescription` | string |  |
| `sku` | string |  |
| `slug` | string |  |
| `soldIndividually` | boolean |  |
| `status` | string |  |
| `stockStatus` | string |  |
| `taxClass` | string |  |
| `taxStatus` | string |  |
| `totalSales` | number |  |
| `virtual` | boolean |  |
| `weight` | string |  |

## Native endpoint

Through the native WooCommerce API, this operation is `POST /products/:productId/duplicate` (base URL `{{credentials.siteUrl}}/wp-json/wc/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-product.md) for the provider-specific parameters and requirements.

