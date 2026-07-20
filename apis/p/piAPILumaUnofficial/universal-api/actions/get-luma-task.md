# PiAPI/Luma (unofficial): Get Luma Task

Retrieves a Luma task from PiAPI.

```
GET https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/get-luma-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Luma (unofficial) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/get-luma-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/get-luma-task?${params}`, {
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
| `taskId` | string | yes | Luma task identifier returned by Create Luma Task. |

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
        "error": {},
        "input": {},
        "logs": [
          "string"
        ],
        "meta": {},
        "model": "string",
        "output": {
          "video": "string"
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
| `code` | number | PiAPI status code. |
| `data` | object | Task payload for the requested task_id. |
| `data.config` | object | Task configuration. |
| `data.detail` | object | Provider detail payload when present. |
| `data.error` | object | Provider error payload when the task fails. |
| `data.input` | object | Submitted generation input. |
| `data.logs` | array<string> | Provider log messages. |
| `data.meta` | object | Provider metadata including timestamps and usage. |
| `data.model` | string | Provider model family. |
| `data.output` | object | Generated output when available. |
| `data.output.video` | string | Generated video URL when the task is completed. |
| `data.status` | string | Current task status. |
| `data.task_id` | string | PiAPI task identifier. |
| `data.task_type` | string | PiAPI task type. |
| `message` | string | PiAPI status message. |

## Native endpoint

Through the native PiAPI/Luma (unofficial) API, this operation is `GET /api/v1/task/:task_id` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-luma-task.md) for the provider-specific parameters and requirements.

