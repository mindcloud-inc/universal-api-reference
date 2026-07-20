# YouCan: List Products

Retrieves a list of products from YouCan.

```
GET https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youCan/latest/actions/list-products?${params}`, {
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
| `inventory` | string | no |  |
| `limit` | string | no |  |
| `page` | string | no |  |
| `q` | string | no |  |
| `sort_field` | string | no |  |
| `sort_order` | string | no |  |
| `trashed` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "compare_at_price": 1,
          "created_at": "2026-05-07T12:00:00.000Z",
          "deleted_at": true,
          "description": "string",
          "has_variants": true,
          "id": "string",
          "images": [
            {
              "id": "string",
              "name": "Ava Chen",
              "order": 1,
              "type": 1,
              "url": "https://example.com",
              "variations": {
                "lg": "string",
                "md": "string",
                "original": "string",
                "sm": "string"
              }
            }
          ],
          "inventory": 1,
          "meta": {
            "description": "string",
            "title": "string"
          },
          "name": "Ava Chen",
          "orders_count": 1,
          "price": 1,
          "public_url": "https://example.com",
          "slug": "string",
          "thumbnail": "string",
          "track_inventory": true,
          "updated_at": "2026-05-07T12:00:00.000Z",
          "variant_options": [
            {
              "name": "Ava Chen",
              "type": 1,
              "values": [
                "string"
              ]
            }
          ],
          "variants_count": 1,
          "visibility": true,
          "you_save_amount": 1
        }
      ],
      "meta": {
        "pagination": {
          "count": 1,
          "current_page": 1,
          "links": {
            "next": "https://example.com"
          },
          "per_page": 1,
          "total": 1,
          "total_pages": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].compare_at_price` | number |  |
| `data[].created_at` | date |  |
| `data[].deleted_at` | boolean |  |
| `data[].description` | string |  |
| `data[].has_variants` | boolean |  |
| `data[].id` | string |  |
| `data[].images` | array<object> |  |
| `data[].images[].id` | string |  |
| `data[].images[].name` | string |  |
| `data[].images[].order` | number |  |
| `data[].images[].type` | number |  |
| `data[].images[].url` | string |  |
| `data[].images[].variations` | object |  |
| `data[].images[].variations.lg` | string |  |
| `data[].images[].variations.md` | string |  |
| `data[].images[].variations.original` | string |  |
| `data[].images[].variations.sm` | string |  |
| `data[].inventory` | number |  |
| `data[].meta` | object |  |
| `data[].meta.description` | string |  |
| `data[].meta.title` | string |  |
| `data[].name` | string |  |
| `data[].orders_count` | number |  |
| `data[].price` | number |  |
| `data[].public_url` | string |  |
| `data[].slug` | string |  |
| `data[].thumbnail` | string |  |
| `data[].track_inventory` | boolean |  |
| `data[].updated_at` | date |  |
| `data[].variant_options` | array<object> |  |
| `data[].variant_options[].name` | string |  |
| `data[].variant_options[].type` | number |  |
| `data[].variant_options[].values` | array<string> |  |
| `data[].variants_count` | number |  |
| `data[].visibility` | boolean |  |
| `data[].you_save_amount` | number |  |
| `meta` | object |  |
| `meta.pagination` | object |  |
| `meta.pagination.count` | number |  |
| `meta.pagination.current_page` | number |  |
| `meta.pagination.links` | object |  |
| `meta.pagination.links.next` | string |  |
| `meta.pagination.per_page` | number |  |
| `meta.pagination.total` | number |  |
| `meta.pagination.total_pages` | number |  |

## Native endpoint

Through the native YouCan API, this operation is `GET /products` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

