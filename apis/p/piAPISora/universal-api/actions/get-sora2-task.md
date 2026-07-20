# PiAPI/Sora: Get Sora2 Task



```
GET https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/get-sora2-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Sora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/get-sora2-task?connectionId=$CONNECTION_ID&taskId=4eba5893-2a39-4218-b5aa-bb9f3c4a26b2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "4eba5893-2a39-4218-b5aa-bb9f3c4a26b2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/get-sora2-task?${params}`, {
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
| `taskId` | string | yes | Task identifier returned by PiAPI. Example: `4eba5893-2a39-4218-b5aa-bb9f3c4a26b2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "error": {
          "code": 1,
          "message": "string",
          "raw_message": "string"
        },
        "input": {
          "aspect_ratio": "string",
          "duration": 1,
          "prompt": "string"
        },
        "meta": {
          "created_at": "2026-05-07T12:00:00.000Z",
          "ended_at": "2026-05-07T12:00:00.000Z",
          "is_using_private_pool": true,
          "started_at": "2026-05-07T12:00:00.000Z",
          "usage": {
            "consume": 1,
            "frozen": 1,
            "type": "string"
          }
        },
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
| `code` | number |  |
| `data.error.code` | number |  |
| `data.error.message` | string |  |
| `data.error.raw_message` | string |  |
| `data.input.aspect_ratio` | string |  |
| `data.input.duration` | number |  |
| `data.input.prompt` | string |  |
| `data.meta.created_at` | date |  |
| `data.meta.ended_at` | date |  |
| `data.meta.is_using_private_pool` | boolean |  |
| `data.meta.started_at` | date |  |
| `data.meta.usage.consume` | number |  |
| `data.meta.usage.frozen` | number |  |
| `data.meta.usage.type` | string |  |
| `data.model` | string |  |
| `data.output.video` | string |  |
| `data.status` | string |  |
| `data.task_id` | string |  |
| `data.task_type` | string |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Sora API, this operation is `GET /api/v1/task/{task_id}` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sora2-task.md) for the provider-specific parameters and requirements.

