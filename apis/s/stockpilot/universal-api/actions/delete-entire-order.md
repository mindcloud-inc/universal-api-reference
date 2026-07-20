# Stockpilot: Delete Entire Order

Deletes an order from Stockpilot.

```
DELETE https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/delete-entire-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/delete-entire-order?connectionId=$CONNECTION_ID&order_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "order_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/delete-entire-order?${params}`, {
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
| `order_id` | number | yes |  |
| `bookBack` | boolean | no | Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Stockpilot API returns.

## Native endpoint

Through the native Stockpilot API, this operation is `DELETE /orders/:order_id` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-entire-order.md) for the provider-specific parameters and requirements.

