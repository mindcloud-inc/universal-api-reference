# JoggAI: Create Video From Avatar



```
POST https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-video-from-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-video-from-avatar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "aspectRatio": "string",
  "avatar.avatar_id": 1,
  "avatar.avatar_type": 1,
  "screenStyle": 1,
  "voice.script": "string",
  "voice.type": "string",
  "voice.voice_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/create-video-from-avatar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "aspectRatio": "string",
    "avatar.avatar_id": 1,
    "avatar.avatar_type": 1,
    "screenStyle": 1,
    "voice.script": "string",
    "voice.type": "string",
    "voice.voice_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aspectRatio` | string | yes | Video aspect ratio: portrait, landscape, or square. |
| `avatar.avatar_id` | number | yes | Avatar ID to use in the video. |
| `avatar.avatar_type` | number | yes | 0 for public avatars, 1 for custom avatars. |
| `caption` | boolean | no | Whether captions should be included in the generated video. |
| `screenStyle` | number | yes | Numeric screen style variant for the output video. |
| `voice.audio_url` | string | no | Public audio URL to use when voice type is audio. |
| `voice.script` | string | yes | Script to speak when voice type is script. |
| `voice.type` | string | yes | Use script for text-to-speech or audio for an uploaded audio URL. |
| `voice.voice_id` | string | yes | Voice ID for text-to-speech generation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `videoId` | string |  |

## Native endpoint

Through the native JoggAI API, this operation is `POST /v2/create_video_from_avatar` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video-from-avatar.md) for the provider-specific parameters and requirements.

