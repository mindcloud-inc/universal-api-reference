# PiAPI/MMAudio: Generate Audio

Creates an MMAudio audio generation task in PiAPI/MMAudio.

```
POST https://connect.mindcloud.co/v1/universal/piAPIMMAudio/latest/actions/generate-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/MMAudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIMMAudio/latest/actions/generate-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.video": "https://example.com/video.mp4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIMMAudio/latest/actions/generate-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.video": "https://example.com/video.mp4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.video` | string | yes | Public video URL to send to PiAPI MMAudio. Example: `https://example.com/video.mp4`. |
| `input.prompt` | string | no | Example: `energetic stadium ambience with crowd cheers`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.negativePrompt` | string | no | Example: `static, clipping, muffled audio`. |
| `input.steps` | number | no | Default: `20`. Example: `20`. |
| `input.seed` | number | no | Example: `48511119825268`. |
| `config.webhookConfig.endpoint` | string | no | Example: `https://example.com/piapi-webhook`. |
| `config.webhookConfig.secret` | string | no | Example: `shared-secret-for-webhook-verification`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {
        "code": 1,
        "message": "string"
      },
      "meta": {
        "createdAt": "string",
        "endedAt": "string",
        "isUsingPrivatePool": true,
        "startedAt": "string",
        "usage": {
          "consume": 1,
          "frozen": 1,
          "type": "string"
        }
      },
      "model": "string",
      "status": "string",
      "taskId": "string",
      "taskType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.code` | number |  |
| `error.message` | string |  |
| `meta.createdAt` | string |  |
| `meta.endedAt` | string |  |
| `meta.isUsingPrivatePool` | boolean |  |
| `meta.startedAt` | string |  |
| `meta.usage.consume` | number |  |
| `meta.usage.frozen` | number |  |
| `meta.usage.type` | string |  |
| `model` | string |  |
| `status` | string |  |
| `taskId` | string |  |
| `taskType` | string |  |

## Native endpoint

Through the native PiAPI/MMAudio API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-audio.md) for the provider-specific parameters and requirements.

