# PiAPI/FaceSwap: Multi Faceswap

Creates a multi-face faceswap task in PiAPI/FaceSwap.

```
POST https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/multi-faceswap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/FaceSwap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/multi-faceswap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.swapImage": "string",
  "input.targetImage": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/multi-faceswap', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.swapImage": "string",
    "input.targetImage": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.swapImage` | string | yes | URL or base64 image containing the source faces. |
| `input.targetImage` | string | yes | URL or base64 image containing the faces to replace. |
| `input.swapFacesIndex` | string | no | Comma-separated source face indexes in PiAPI's detected order. |
| `input.targetFacesIndex` | string | no | Comma-separated target face indexes in PiAPI's detected order. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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
        "detail": {},
        "error": {
          "code": 1,
          "detail": {},
          "message": "string",
          "raw_message": "string"
        },
        "input": {},
        "logs": [
          {}
        ],
        "meta": {},
        "model": "string",
        "output": {},
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
| `data.detail` | object | Provider task detail payload when present. |
| `data.error` | object | Provider error payload. |
| `data.error.code` | number | Provider error code. |
| `data.error.detail` | object | Provider error detail payload when present. |
| `data.error.message` | string | Provider error message. |
| `data.error.raw_message` | string | Raw provider error message. |
| `data.input` | object | Task input payload. |
| `data.logs` | array<object> | Provider task logs. |
| `data.meta` | object | Task metadata payload. |
| `data.model` | string | PiAPI model name. |
| `data.output` | object | Task output payload when available. |
| `data.status` | string | Initial task status. |
| `data.task_id` | string | Created PiAPI task identifier. |
| `data.task_type` | string | PiAPI task type. |
| `message` | string | PiAPI response message. |

## Native endpoint

Through the native PiAPI/FaceSwap API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/multi-faceswap.md) for the provider-specific parameters and requirements.

