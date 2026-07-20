# Pastefy: Delete API Key



```
DELETE https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/delete-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pastefy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/delete-api-key?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/delete-api-key?${params}`, {
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
| `id` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pastefy API returns.

## Native endpoint

Through the native Pastefy API, this operation is `DELETE /user/keys/:id` (base URL `https://pastefy.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-api-key.md) for the provider-specific parameters and requirements.

