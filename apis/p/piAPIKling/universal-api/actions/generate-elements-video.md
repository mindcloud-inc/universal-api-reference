# PiAPI/Kling: Generate Elements Video



```
POST https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-elements-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Kling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-elements-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "string",
  "input.duration": 1,
  "input.elements[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-elements-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "string",
    "input.duration": 1,
    "input.elements[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.prompt` | string | yes | Describe the desired elements-based video output. |
| `input.negativePrompt` | string | no | Describe what Kling should avoid in the elements video. |
| `input.duration` | number | yes | Elements video length in seconds, typically 5 or 10. |
| `input.aspectRatio` | string | no | Output aspect ratio such as 16:9, 9:16, or 1:1. |
| `input.mode` | string | no | Elements generation mode, such as std. |
| `input.elements[]` | array<object> | yes | Array of 1-4 element objects, each with an image_url field. |

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

Through the native PiAPI/Kling API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-elements-video.md) for the provider-specific parameters and requirements.

