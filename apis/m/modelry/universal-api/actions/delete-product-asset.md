# Modelry: Delete Product Asset



```
DELETE https://connect.mindcloud.co/v1/universal/modelry/latest/actions/delete-product-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modelry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/modelry/latest/actions/delete-product-asset?connectionId=$CONNECTION_ID&productId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modelry/latest/actions/delete-product-asset?${params}`, {
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
| `productId` | number | yes | Modelry product ID. |
| `id` | number | yes | Modelry product asset ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Modelry API returns.

## Native endpoint

Through the native Modelry API, this operation is `DELETE /v1/products/:product_id/assets/:id` (base URL `https://api.modelry.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-product-asset.md) for the provider-specific parameters and requirements.

