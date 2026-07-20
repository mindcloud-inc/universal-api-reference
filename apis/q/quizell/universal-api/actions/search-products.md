# Quizell: Search Products

Finds products in Quizell by title or SKU.

```
GET https://connect.mindcloud.co/v1/universal/quizell/latest/actions/search-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quizell `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/search-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quizell/latest/actions/search-products?${params}`, {
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
| `title` | string | no | Product title to search for. |
| `sku` | string | no | Product SKU to search for. |
| `status` | number | no | Product status: 1 for active, 0 for inactive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bullet_description": "string",
      "collections": [
        {}
      ],
      "compare_at_price": 1,
      "created_at": "string",
      "description": "string",
      "detail_link": "https://example.com",
      "id": 1,
      "image": "string",
      "images": [
        {}
      ],
      "price": "string",
      "sku": "string",
      "status": true,
      "tags": [
        "string"
      ],
      "title": "string",
      "updated_at": "string",
      "vendor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bullet_description` | string |  |
| `collections` | array<object> |  |
| `compare_at_price` | number |  |
| `created_at` | string |  |
| `description` | string |  |
| `detail_link` | string |  |
| `id` | number |  |
| `image` | string |  |
| `images` | array<object> |  |
| `price` | string |  |
| `sku` | string |  |
| `status` | boolean |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `updated_at` | string |  |
| `vendor` | string |  |

## Native endpoint

Through the native Quizell API, this operation is `GET /products/search` (base URL `https://api.quizell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-products.md) for the provider-specific parameters and requirements.

