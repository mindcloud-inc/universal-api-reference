# Fish Audio: Update Model

Updates an existing voice model in Fish Audio.

```
PUT https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/update-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fish Audio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/update-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/update-model', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Fish Audio model ID. |
| `title` | string | no | Updated model title. |
| `description` | string | no | Updated model description. |
| `coverImage` | file | no | Updated model cover image. |
| `visibility` | list | no | Updated model visibility. One of: `0`, `1`, `2`. |
| `tags[]` | array<string> | no | Updated model tags. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fish Audio API returns.

## Native endpoint

Through the native Fish Audio API, this operation is `PATCH /model/:id` (base URL `https://api.fish.audio`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-model.md) for the provider-specific parameters and requirements.

