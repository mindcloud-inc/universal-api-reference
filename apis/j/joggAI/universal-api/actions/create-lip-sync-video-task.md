# JoggAI: Create Lip Sync Video Task



```
POST https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-lip-sync-video-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-lip-sync-video-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audioUrl": "https://example.com",
  "videoUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-lip-sync-video-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audioUrl": "https://example.com",
    "videoUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audioUrl` | string | yes | Source audio URL |
| `playbackType` | string | no | Playback strategy when the source video is shorter than the audio Default: `normal`. |
| `videoUrl` | string | yes | Source video URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Initial lip sync task status |
| `taskId` | string | Created lip sync task identifier |

## Native endpoint

Through the native JoggAI API, this operation is `POST /v2/create_lip_sync_video` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lip-sync-video-task.md) for the provider-specific parameters and requirements.

