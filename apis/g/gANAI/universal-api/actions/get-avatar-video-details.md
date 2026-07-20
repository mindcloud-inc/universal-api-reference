# GAN.AI: Get Avatar Video Details

Retrieves details for an avatar video in GAN.AI.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-avatar-video-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-avatar-video-details?connectionId=$CONNECTION_ID&inferenceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inferenceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-avatar-video-details?${params}`, {
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
| `inferenceId` | string | yes |  |

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
      "videoMetadata": {
        "duration": 1,
        "orientation": "string"
      },
      "videos": {
        "default": "string",
        "landscape": "string",
        "portrait": "string"
      }
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
| `videoMetadata.duration` | number |  |
| `videoMetadata.orientation` | string |  |
| `videos.default` | string |  |
| `videos.landscape` | string |  |
| `videos.portrait` | string |  |

## Native endpoint

Through the native GAN.AI API, this operation is `GET /v1/avatars/inference_details` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-avatar-video-details.md) for the provider-specific parameters and requirements.

