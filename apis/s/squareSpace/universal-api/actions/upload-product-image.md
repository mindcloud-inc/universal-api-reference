# SquareSpace: Upload Product Image

Uploads a product image to Squarespace.

```
POST https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/upload-product-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/upload-product-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/upload-product-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Image file binary payload. |
| `id` | list<string> | yes | Product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageId` | string |  |

## Native endpoint

Through the native SquareSpace API, this operation is `POST /v2/commerce/products/:id/images` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-product-image.md) for the provider-specific parameters and requirements.

