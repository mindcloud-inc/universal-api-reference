# SquareSpace: Delete Product Variant

Deletes a product variant from Squarespace.

```
DELETE https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/delete-product-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/delete-product-variant?connectionId=$CONNECTION_ID&productId=string&variantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string",
  "variantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/delete-product-variant?${params}`, {
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
| `productId` | list<string> | yes | Product ID. |
| `variantId` | list<string> | yes | Variant ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SquareSpace API returns.

## Native endpoint

Through the native SquareSpace API, this operation is `DELETE /v2/commerce/products/:productId/variants/:variantId` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-product-variant.md) for the provider-specific parameters and requirements.

