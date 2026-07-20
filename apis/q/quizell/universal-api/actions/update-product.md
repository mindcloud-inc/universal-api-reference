# Quizell: Update Product

Updates an existing product in Quizell.

```
PUT https://connect.mindcloud.co/v1/universal/quizell/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quizell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quizell/latest/actions/update-product', {
  method: 'PUT',
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
| `productId` | number | yes | The ID of the product to update. |
| `status` | boolean | no | Product active status. |
| `title` | string | no | Product title. |
| `price` | number | no | Product price. |
| `description` | string | no | Product description. |
| `image` | string | no | Product image URL. |
| `tags[]` | array<string> | no | Product tags. |
| `sku` | string | no | Product SKU. |

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

Through the native Quizell API, this operation is `PUT /products/update/:product_id` (base URL `https://api.quizell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

