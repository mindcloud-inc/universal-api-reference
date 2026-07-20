# WeForest: Delete order item

Deletes an existing tree-planting order item from WeForest.

```
DELETE https://connect.mindcloud.co/v1/universal/weForest/latest/actions/delete-order-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeForest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/delete-order-item?connectionId=$CONNECTION_ID&orderId=1&itemId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1",
  "itemId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weForest/latest/actions/delete-order-item?${params}`, {
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
| `orderId` | number | yes | Order identifier from WeForest. |
| `itemId` | number | yes | Order item identifier from WeForest. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WeForest API returns.

## Native endpoint

Through the native WeForest API, this operation is `DELETE /trees/:orderId/items/:itemId` (base URL `https://api.weforest.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-order-item.md) for the provider-specific parameters and requirements.

