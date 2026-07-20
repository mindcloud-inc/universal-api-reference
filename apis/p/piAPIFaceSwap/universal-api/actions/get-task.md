# PiAPI/FaceSwap: Get Task

Retrieves a task from PiAPI/FaceSwap by ID.

```
GET https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/FaceSwap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/get-task?${params}`, {
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
| `taskId` | string | yes | The PiAPI task identifier to retrieve. |

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
| `data.status` | string | Current task status. |
| `data.task_id` | string | PiAPI task identifier. |
| `data.task_type` | string | PiAPI task type. |
| `message` | string | PiAPI response message. |

## Native endpoint

Through the native PiAPI/FaceSwap API, this operation is `GET /api/v1/task/{task_id}` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

