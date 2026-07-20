# Easy-Peasy.AI: Generate Talking Video

Generates a talking video in Easy-Peasy.AI.

```
POST https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/generate-talking-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy-Peasy.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/generate-talking-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/generate-talking-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image` | string | no | Optional face image URL to animate. |
| `video` | string | no | Optional source video URL to lip-sync. |
| `text` | string | no | Optional speech text when you are not providing an audio file. |
| `voiceId` | string | no | Optional TTS voice identifier when using text input. |
| `audio` | string | no | Optional audio file URL to use directly. |
| `avatarModel` | string | no | Optional avatar generation mode for image-based talking videos. |
| `resolution` | string | no | Optional output resolution for the talking video. |
| `generateCaptions` | boolean | no | Whether to generate captions on the output video. |
| `captionColor` | string | no | Optional caption highlight color in hex format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Easy-Peasy.AI API returns.

## Native endpoint

Through the native Easy-Peasy.AI API, this operation is `POST /api/generate-talking-video` (base URL `https://easy-peasy.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-talking-video.md) for the provider-specific parameters and requirements.

