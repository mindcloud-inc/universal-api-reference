# Simplecast: Upload Episode Audio

Uploads episode audio to Simplecast.

```
POST https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/upload-episode-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplecast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/upload-episode-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audioUrl": "https://example.com",
  "episodeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/upload-episode-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audioUrl": "https://example.com",
    "episodeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audioUrl` | string | yes | Publicly reachable audio file URL to attach to the episode. |
| `episodeId` | string | yes | Simplecast episode identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "fileName": "Ava Chen",
      "href": "string",
      "id": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `fileName` | string |  |
| `href` | string |  |
| `id` | string |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Simplecast API, this operation is `POST /episodes/:episode_id/audio` (base URL `https://api.simplecast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-episode-audio.md) for the provider-specific parameters and requirements.

