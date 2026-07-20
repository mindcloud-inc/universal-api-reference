# SquareSpace: Update Product Image

Updates a product image in Squarespace.

```
PUT https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/update-product-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/update-product-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageId": "string",
  "productId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/update-product-image', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageId": "string",
    "productId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageId` | string | yes | Image ID. |
| `productId` | list<string> | yes | Product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altText": "string",
      "availableFormats": [
        {}
      ],
      "id": "string",
      "orderIndex": 1,
      "originalSize": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altText` | string |  |
| `availableFormats` | array<object> |  |
| `id` | string |  |
| `orderIndex` | number |  |
| `originalSize` | object |  |
| `url` | string |  |

## Native endpoint

Through the native SquareSpace API, this operation is `POST /v2/commerce/products/:productId/images/:imageId` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-image.md) for the provider-specific parameters and requirements.

