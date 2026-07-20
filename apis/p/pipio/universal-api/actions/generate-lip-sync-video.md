# Pipio: Generate Lip Sync Video

Creates a lip-synced video in Pipio from source video and audio.

```
POST https://connect.mindcloud.co/v1/universal/pipio/latest/actions/generate-lip-sync-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipio/latest/actions/generate-lip-sync-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceUrl": "https://cdn.pipio.ai/your-video.mp4",
  "targetAudioUrl": "https://cdn.pipio.ai/your-audio.mpga"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipio/latest/actions/generate-lip-sync-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceUrl": "https://cdn.pipio.ai/your-video.mp4",
    "targetAudioUrl": "https://cdn.pipio.ai/your-audio.mpga"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceUrl` | string | yes | The URL to your source video that will be lip-synced. Example: `https://cdn.pipio.ai/your-video.mp4`. |
| `targetAudioUrl` | string | yes | The URL to the audio file that will be synced to the video. Example: `https://cdn.pipio.ai/your-audio.mpga`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bypassEditing": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bypassEditing` | boolean | Whether the project bypassed manual editing. |
| `id` | string | Generated lip sync project id. |

## Native endpoint

Through the native Pipio API, this operation is `POST https://project.pipio.ai/project/generate/lipsync` (base URL `https://avatar.pipio.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-lip-sync-video.md) for the provider-specific parameters and requirements.

