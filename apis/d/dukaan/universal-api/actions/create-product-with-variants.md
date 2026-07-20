# Dukaan: Create Product With Variants

Creates a new product with variants in Dukaan.

```
POST https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-product-with-variants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-product-with-variants" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storeUuid": "your-store-uuid",
  "name": "Sample Product With Variants",
  "sellingPrice": "90",
  "store": "your-store-uuid",
  "skus[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-product-with-variants', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "storeUuid": "your-store-uuid",
    "name": "Sample Product With Variants",
    "sellingPrice": "90",
    "store": "your-store-uuid",
    "skus[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `storeUuid` | string | yes | Dukaan store UUID from developer settings. Example: `your-store-uuid`. |
| `name` | string | yes | Product name. Example: `Sample Product With Variants`. |
| `sellingPrice` | number | yes | Product selling price. Example: `90`. |
| `originalPrice` | number | no | Product original price. Example: `100`. |
| `unit` | string | no | Product unit. Default: `piece`. |
| `description` | string | no | Product description HTML. Example: `Product description`. |
| `categories[]` | array<number> | no | Category IDs for the product. |
| `store` | string | yes | Store UUID for the product body. Example: `your-store-uuid`. |
| `skus[]` | array<object> | yes | Variant SKU objects. |
| `inStock` | boolean | no | Whether the product is in stock. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "all_images": [
        "string"
      ],
      "base_qty": 1,
      "categories_data": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "image": "string",
      "in_stock": true,
      "inventory_quantity": 1,
      "is_active": true,
      "name": "Ava Chen",
      "original_price": 1,
      "selling_price": 1,
      "slug": "string",
      "unit": "string",
      "uuid": "string",
      "web_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `all_images` | array<string> | Product image URLs |
| `base_qty` | number | Base quantity |
| `categories_data` | array<object> | Associated categories |
| `created_at` | date | Creation timestamp |
| `id` | number | Dukaan product ID |
| `image` | string | Primary image URL |
| `in_stock` | boolean | Whether the product is in stock |
| `inventory_quantity` | number | Available inventory quantity |
| `is_active` | boolean | Whether the product is active |
| `name` | string | Product name |
| `original_price` | number | Original price |
| `selling_price` | number | Selling price |
| `slug` | string | Product slug |
| `unit` | string | Product unit |
| `uuid` | string | Dukaan product UUID |
| `web_url` | string | Storefront product URL |

## Native endpoint

Through the native Dukaan API, this operation is `POST api/product/seller/:storeUuid/product/v2/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product-with-variants.md) for the provider-specific parameters and requirements.

