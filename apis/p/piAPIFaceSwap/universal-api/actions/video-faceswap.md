# PiAPI/FaceSwap: Video Faceswap

Creates a video faceswap task in PiAPI/FaceSwap.

```
POST https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/video-faceswap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/FaceSwap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/video-faceswap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.swapImage": "string",
  "input.targetVideo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/video-faceswap', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.swapImage": "string",
    "input.targetVideo": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.swapImage` | string | yes | URL or base64 image containing the replacement face or faces. |
| `input.targetVideo` | string | yes | MP4 video URL to process. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.swapFacesIndex` | string | no | Optional source face indexes for multi-face video swaps. |
| `input.targetFacesIndex` | string | no | Optional target face indexes for multi-face video swaps. |
| `config.webhookConfig.endpoint` | string | no | Optional webhook URL for task status notifications. |
| `config.webhookConfig.secret` | string | no | Optional webhook secret returned as x-webhook-secret. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "config": {},
        "error": {
          "code": 1,
          "detail": {},
          "message": "string",
          "raw_message": "string"
        },
        "input": {},
        "meta": {},
        "model": "string",
        "output": {
          "video_url": "https://example.com"
        },
        "status": "string",
        "task_id": "string",
        "task_type": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | PiAPI response code. |
| `data` | object | Unified PiAPI task response payload. |
| `data.config` | object | Task configuration payload. |
| `data.error` | object | Provider error payload. |
| `data.error.code` | number | Provider error code. |
| `data.error.detail` | object | Provider error detail payload when present. |
| `data.error.message` | string | Provider error message. |
| `data.error.raw_message` | string | Raw provider error message. |
| `data.input` | object | Task input payload. |
| `data.meta` | object | Task metadata payload. |
| `data.model` | string | PiAPI model name. |
| `data.output` | object | Task output payload when available. |
| `data.output.video_url` | string | Rendered video URL when available. |
| `data.status` | string | Initial task status. |
| `data.task_id` | string | Created PiAPI task identifier. |
| `data.task_type` | string | PiAPI task type. |
| `message` | string | PiAPI response message. |

## Native endpoint

Through the native PiAPI/FaceSwap API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/video-faceswap.md) for the provider-specific parameters and requirements.

