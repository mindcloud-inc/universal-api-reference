# SquareSpace: Delete Product Image

Deletes a product image from Squarespace.

```
DELETE https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/delete-product-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/delete-product-image?connectionId=$CONNECTION_ID&imageId=string&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageId": "string",
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/delete-product-image?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SquareSpace API returns.

## Native endpoint

Through the native SquareSpace API, this operation is `DELETE /v2/commerce/products/:productId/images/:imageId` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-product-image.md) for the provider-specific parameters and requirements.

