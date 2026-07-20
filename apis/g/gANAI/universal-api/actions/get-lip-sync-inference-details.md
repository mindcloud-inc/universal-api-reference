# GAN.AI: Get LipSync Inference Details

Retrieves details for a lip-sync inference in GAN.AI.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-lip-sync-inference-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-lip-sync-inference-details?connectionId=$CONNECTION_ID&inferenceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inferenceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-lip-sync-inference-details?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "downloadableVideoUrl": "https://example.com",
      "inferenceId": "string",
      "inputAudio": "string",
      "inputVideo": "string",
      "status": "string",
      "thumbnailUrl": "https://example.com",
      "title": "string",
      "useAudioFromVideo": true,
      "videoUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `downloadableVideoUrl` | string |  |
| `inferenceId` | string |  |
| `inputAudio` | string |  |
| `inputVideo` | string |  |
| `status` | string |  |
| `thumbnailUrl` | string |  |
| `title` | string |  |
| `useAudioFromVideo` | boolean |  |
| `videoUrl` | string |  |

## Native endpoint

Through the native GAN.AI API, this operation is `GET /v1/lipsync/inference_details` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lip-sync-inference-details.md) for the provider-specific parameters and requirements.

