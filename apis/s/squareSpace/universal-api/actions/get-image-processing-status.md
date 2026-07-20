# SquareSpace: Get Image Processing Status

Retrieves product image processing status from Squarespace.

```
GET https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-image-processing-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-image-processing-status?connectionId=$CONNECTION_ID&imageId=string&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageId": "string",
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-image-processing-status?${params}`, {
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
| `imageId` | string | yes | Image ID. |
| `productId` | list<string> | yes | Product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native SquareSpace API, this operation is `GET /v2/commerce/products/:productId/images/:imageId/status` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image-processing-status.md) for the provider-specific parameters and requirements.

