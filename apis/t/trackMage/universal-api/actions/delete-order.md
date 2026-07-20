# TrackMage: Delete Order

Deletes an existing order from TrackMage.

```
DELETE https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/delete-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/delete-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/delete-order?${params}`, {
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
| `id` | string | yes | Resource identifier |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TrackMage API returns.

## Native endpoint

Through the native TrackMage API, this operation is `DELETE /orders/{id}` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-order.md) for the provider-specific parameters and requirements.

