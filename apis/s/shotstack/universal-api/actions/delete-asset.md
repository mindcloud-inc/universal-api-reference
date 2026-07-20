# Shotstack: Delete Asset



```
DELETE https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/delete-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shotstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/delete-asset?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/delete-asset?${params}`, {
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
| `id` | string | yes | The Shotstack asset ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shotstack API returns.

## Native endpoint

Through the native Shotstack API, this operation is `DELETE /serve/v1/assets/:id` (base URL `https://api.shotstack.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-asset.md) for the provider-specific parameters and requirements.

