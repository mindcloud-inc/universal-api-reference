# SquareSpace: Update Product

Updates a product in Squarespace.

```
PUT https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | list<string> | yes | Product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "string",
      "description": "string",
      "id": "string",
      "images": [
        {}
      ],
      "isVisible": true,
      "modifiedOn": "string",
      "name": "Ava Chen",
      "seoOptions": {},
      "storePageId": "string",
      "tags": [
        "string"
      ],
      "type": "string",
      "url": "https://example.com",
      "urlSlug": "https://example.com",
      "variantAttributes": [
        "string"
      ],
      "variants": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | string |  |
| `description` | string |  |
| `id` | string |  |
| `images` | array<object> |  |
| `isVisible` | boolean |  |
| `modifiedOn` | string |  |
| `name` | string |  |
| `seoOptions` | object |  |
| `storePageId` | string |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `url` | string |  |
| `urlSlug` | string |  |
| `variantAttributes` | array<string> |  |
| `variants` | array<object> |  |

## Native endpoint

Through the native SquareSpace API, this operation is `POST /v2/commerce/products/:id` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

