# GAN.AI: Create Photo Avatar Inference

Creates a talking-head video for a photo avatar in GAN.AI.

```
POST https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/create-photo-avatar-inference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/create-photo-avatar-inference" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "photoAvatarId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/create-photo-avatar-inference', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "photoAvatarId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audioUrl` | string | no |  |
| `photoAvatarId` | string | yes |  |
| `text` | string | no |  |
| `title` | string | no |  |
| `voiceSampleUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioData": {
        "audioS3Key": "string",
        "inputAudioUrl": "https://example.com",
        "inputText": "string",
        "isTtsInference": true,
        "ttsInferenceId": "string",
        "voiceCloneUrl": "https://example.com",
        "voiceId": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "photoAvatarId": "string",
      "photoAvatarInferenceId": "string",
      "status": "string",
      "title": "string",
      "video": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioData.audioS3Key` | string |  |
| `audioData.inputAudioUrl` | string |  |
| `audioData.inputText` | string |  |
| `audioData.isTtsInference` | boolean |  |
| `audioData.ttsInferenceId` | string |  |
| `audioData.voiceCloneUrl` | string |  |
| `audioData.voiceId` | string |  |
| `createdAt` | date |  |
| `photoAvatarId` | string |  |
| `photoAvatarInferenceId` | string |  |
| `status` | string |  |
| `title` | string |  |
| `video` | string |  |

## Native endpoint

Through the native GAN.AI API, this operation is `POST /v1/photo_avatars/create_inference` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-photo-avatar-inference.md) for the provider-specific parameters and requirements.

