# Vooplayer: Update Video Player Settings

Updates video player settings in Vooplayer.

```
PUT https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/update-video-player-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vooplayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/update-video-player-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "settings": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/update-video-player-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "settings": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Video ID as the base64 decoded value. |
| `settings` | object | yes | Object containing only the keys to update. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vooplayer API returns.

## Native endpoint

Through the native Vooplayer API, this operation is `POST /video/updateSettings` (base URL `https://api.spotlightr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-video-player-settings.md) for the provider-specific parameters and requirements.

