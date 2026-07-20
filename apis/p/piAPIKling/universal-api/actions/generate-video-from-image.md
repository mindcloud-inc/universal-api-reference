# PiAPI/Kling: Generate Video from Image



```
POST https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-video-from-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Kling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-video-from-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.imageUrl": "https://example.com",
  "input.prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-video-from-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.imageUrl": "https://example.com",
    "input.prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.imageUrl` | string | yes | Source image URL for image-to-video generation. |
| `input.prompt` | string | yes | Describe the motion or scene you want Kling to generate from the image. |
| `input.negativePrompt` | string | no | Describe what Kling should avoid in the output. |
| `input.imageTailUrl` | string | no | Optional ending frame image URL when supported by the selected Kling version. |
| `input.duration` | number | no | Video length in seconds when supported by the selected Kling version and mode. |
| `input.aspectRatio` | string | no | Output aspect ratio such as 16:9, 9:16, or 1:1. |
| `input.mode` | string | no | Kling generation mode, such as std or pro. |
| `input.version` | string | no | Kling version, such as 1.6, 2.5, or 2.6. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "detail": {},
      "error": {},
      "input": {},
      "logs": [
        {}
      ],
      "meta": {},
      "model": "string",
      "output": {},
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
| `config` | object | Resolved task configuration. |
| `detail` | object | Provider detail payload when available. |
| `error` | object | Provider error payload. |
| `input` | object | Submitted task input payload. |
| `logs` | array<object> | Task log entries when available. |
| `meta` | object | Task timestamps and usage metadata. |
| `model` | string | Provider model name. |
| `output` | object | Provider output payload. |
| `status` | string | Current task status. |
| `taskId` | string | PiAPI task identifier. |
| `taskType` | string | PiAPI task type. |

## Native endpoint

Through the native PiAPI/Kling API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-video-from-image.md) for the provider-specific parameters and requirements.

