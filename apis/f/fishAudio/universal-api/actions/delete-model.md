# Fish Audio: Delete Model

Deletes an existing voice model from Fish Audio.

```
DELETE https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/delete-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fish Audio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/delete-model?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/delete-model?${params}`, {
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
| `id` | string | yes | The Fish Audio model ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fish Audio API returns.

## Native endpoint

Through the native Fish Audio API, this operation is `DELETE /model/:id` (base URL `https://api.fish.audio`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-model.md) for the provider-specific parameters and requirements.

