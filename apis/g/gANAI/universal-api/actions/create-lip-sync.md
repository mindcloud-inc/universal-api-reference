# GAN.AI: Create LipSync

Creates a lip-sync video in GAN.AI.

```
POST https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/create-lip-sync
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/create-lip-sync" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputs.inputAudioUrl": "https://example.com",
  "inputs.inputVideoUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/create-lip-sync', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputs.inputAudioUrl": "https://example.com",
    "inputs.inputVideoUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no |  |
| `inputs.inputAudioUrl` | string | yes |  |
| `inputs.inputVideoUrl` | string | yes |  |
| `inputs.useAudioFromVideo` | boolean | no |  |
| `title` | string | no |  |

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

Through the native GAN.AI API, this operation is `POST /v1/lipsync/create_lipsync` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lip-sync.md) for the provider-specific parameters and requirements.

