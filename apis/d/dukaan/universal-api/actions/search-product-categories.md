# Dukaan: Search Product Categories

Finds product categories in Dukaan by search query.

```
GET https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/search-product-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/search-product-categories?connectionId=$CONNECTION_ID&limit=25&offset=0&search=Sample%20Category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "search": "Sample Category"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/search-product-categories?${params}`, {
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
| `search` | string | yes | Category search text. Example: `Sample Category`. |

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

Through the native Dukaan API, this operation is `GET api/product/seller/product-category/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-product-categories.md) for the provider-specific parameters and requirements.

