# Dukaan: Create Product Category

Creates a new product category in Dukaan.

```
POST https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-product-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-product-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Summer Collection",
  "store": "your-store-uuid"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/create-product-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Summer Collection",
    "store": "your-store-uuid"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Category name. Example: `Summer Collection`. |
| `store` | string | yes | Store UUID or ID for the category. Example: `your-store-uuid`. |
| `showTo` | number | no | Dukaan visibility value for the category. Default: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "image": "string",
      "in_stock": true,
      "is_active": true,
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "position": 1,
      "product_count": 1,
      "seo_data": {},
      "show_to": 1,
      "slug": "string",
      "sub_categories": [
        {}
      ],
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
| `created_at` | date | Creation timestamp |
| `description` | string | Category description |
| `id` | number | Dukaan category ID |
| `image` | string | Category image URL |
| `in_stock` | boolean | Whether the category has stock |
| `is_active` | boolean | Whether the category is active |
| `modified_at` | date | Last modified timestamp |
| `name` | string | Category name |
| `position` | number | Category sort position |
| `product_count` | number | Number of products in the category |
| `seo_data` | object | SEO metadata |
| `show_to` | number | Audience visibility setting |
| `slug` | string | Category slug |
| `sub_categories` | array<object> | Nested subcategories |
| `uuid` | string | Dukaan category UUID |
| `web_url` | string | Storefront category URL |

## Native endpoint

Through the native Dukaan API, this operation is `POST api/product/seller/product-category/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product-category.md) for the provider-specific parameters and requirements.

