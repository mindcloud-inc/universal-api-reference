# Dukaan: Search Products

Finds products in Dukaan by search query.

```
GET https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/search-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/search-products?connectionId=$CONNECTION_ID&limit=25&offset=0&storeUuid=your-store-uuid&search=Hair%20Pins" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "storeUuid": "your-store-uuid",
  "search": "Hair Pins"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/search-products?${params}`, {
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
| `storeUuid` | string | yes | Dukaan store UUID from developer settings. Example: `your-store-uuid`. |
| `search` | string | yes | Product search text. Example: `Hair Pins`. |

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

Through the native Dukaan API, this operation is `GET api/seller-front/:storeUuid/product-list/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-products.md) for the provider-specific parameters and requirements.

