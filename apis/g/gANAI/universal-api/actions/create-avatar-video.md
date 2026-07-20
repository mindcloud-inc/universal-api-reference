# GAN.AI: Create Avatar Video

Creates an avatar video in GAN.AI.

```
POST https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/create-avatar-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/create-avatar-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "avatarId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/create-avatar-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "avatarId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audioUrl` | string | no |  |
| `avatarId` | string | yes |  |
| `text` | string | no |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioUrl": "https://example.com",
      "avatarId": "string",
      "avatarTitle": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "downloadableSegmentationVideoLinks": "https://example.com",
      "downloadableVideoLink": "https://example.com",
      "downloadableVideoLinks": "https://example.com",
      "inferenceId": "string",
      "inputText": "string",
      "segmentationVideos": "string",
      "status": "string",
      "thumbnail": "string",
      "title": "string",
      "ttsInferenceId": "string",
      "video": "string",
      "videoMetadata": "string",
      "videos": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioUrl` | string |  |
| `avatarId` | string |  |
| `avatarTitle` | string |  |
| `createdAt` | date |  |
| `downloadableSegmentationVideoLinks` | string |  |
| `downloadableVideoLink` | string |  |
| `downloadableVideoLinks` | string |  |
| `inferenceId` | string |  |
| `inputText` | string |  |
| `segmentationVideos` | string |  |
| `status` | string |  |
| `thumbnail` | string |  |
| `title` | string |  |
| `ttsInferenceId` | string |  |
| `video` | string |  |
| `videoMetadata` | string |  |
| `videos` | string |  |

## Native endpoint

Through the native GAN.AI API, this operation is `POST /v1/avatars/create_video` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-avatar-video.md) for the provider-specific parameters and requirements.

