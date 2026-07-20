# YouCan: Get Product

Retrieves details for a product from YouCan.

```
GET https://connect.mindcloud.co/v1/universal/youCan/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouCan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youCan/latest/actions/get-product?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youCan/latest/actions/get-product?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compare_at_price` | number |  |
| `created_at` | date |  |
| `deleted_at` | boolean |  |
| `description` | string |  |
| `has_variants` | boolean |  |
| `id` | string |  |
| `images` | array<object> |  |
| `images[].id` | string |  |
| `images[].name` | string |  |
| `images[].order` | number |  |
| `images[].type` | number |  |
| `images[].url` | string |  |
| `images[].variations` | object |  |
| `images[].variations.lg` | string |  |
| `images[].variations.md` | string |  |
| `images[].variations.original` | string |  |
| `images[].variations.sm` | string |  |
| `inventory` | number |  |
| `meta` | object |  |
| `meta.description` | string |  |
| `meta.title` | string |  |
| `name` | string |  |
| `price` | number |  |
| `public_url` | string |  |
| `slug` | string |  |
| `thumbnail` | string |  |
| `track_inventory` | boolean |  |
| `updated_at` | date |  |
| `variant_options` | array<object> |  |
| `variant_options[].name` | string |  |
| `variant_options[].type` | number |  |
| `variant_options[].values` | array<string> |  |
| `variants_count` | number |  |
| `visibility` | boolean |  |
| `you_save_amount` | number |  |

## Native endpoint

Through the native YouCan API, this operation is `GET /products/{id}` (base URL `https://api.youcan.shop`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

