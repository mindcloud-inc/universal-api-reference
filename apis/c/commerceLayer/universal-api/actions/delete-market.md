# Commerce Layer: Delete Market



```
DELETE https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/delete-market
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/delete-market?connectionId=$CONNECTION_ID&id=VgWXOhKylz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "VgWXOhKylz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/delete-market?${params}`, {
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
| `id` | string | yes | The market ID to delete. Example: `VgWXOhKylz`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Commerce Layer API returns.

## Native endpoint

Through the native Commerce Layer API, this operation is `DELETE /api/markets/:id` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-market.md) for the provider-specific parameters and requirements.

