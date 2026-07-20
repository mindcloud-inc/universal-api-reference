# Quizell: Create Product

Creates a new product in Quizell.

```
POST https://connect.mindcloud.co/v1/universal/quizell/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quizell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "status": true,
  "title": "string",
  "price": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quizell/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "status": true,
    "title": "string",
    "price": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | boolean | yes | Product active status. |
| `title` | string | yes | Product title. |
| `price` | number | yes | Product price. |
| `description` | string | no | Product description. |
| `image` | string | no | Product image URL. |
| `tags[]` | array<string> | no | Product tags. |
| `sku` | string | no | Product SKU. |
| `quantity` | number | no | Available quantity. |

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

Through the native Quizell API, this operation is `POST /products/store` (base URL `https://api.quizell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

