# PiAPI/Skyreels: Get Skyreels Task

Retrieves a Skyreels task by ID from PiAPI.

```
GET https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/get-skyreels-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Skyreels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/get-skyreels-task?connectionId=$CONNECTION_ID&taskId=736fde4d-9029-4915-8189-01353d6982cb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "736fde4d-9029-4915-8189-01353d6982cb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/get-skyreels-task?${params}`, {
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
| `taskId` | string | yes | Skyreels task identifier returned from Create Skyreels Task. Example: `736fde4d-9029-4915-8189-01353d6982cb`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "config": {
          "service_mode": "string",
          "webhook_config": {
            "endpoint": "string",
            "secret": "string"
          }
        },
        "error": {
          "code": 1,
          "message": "string",
          "raw_message": "string"
        },
        "input": {
          "aspect_ratio": "string",
          "guidance_scale": 1,
          "image": "string",
          "negative_prompt": "string",
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
| `code` | number |  |
| `data.config.service_mode` | string |  |
| `data.config.webhook_config.endpoint` | string |  |
| `data.config.webhook_config.secret` | string |  |
| `data.error.code` | number |  |
| `data.error.message` | string |  |
| `data.error.raw_message` | string |  |
| `data.input.aspect_ratio` | string |  |
| `data.input.guidance_scale` | number |  |
| `data.input.image` | string |  |
| `data.input.negative_prompt` | string |  |
| `data.input.prompt` | string |  |
| `data.meta.created_at` | date |  |
| `data.meta.ended_at` | date |  |
| `data.meta.is_using_private_pool` | boolean |  |
| `data.meta.started_at` | date |  |
| `data.meta.usage.consume` | number |  |
| `data.meta.usage.frozen` | number |  |
| `data.meta.usage.type` | string |  |
| `data.model` | string |  |
| `data.output.video_url` | string |  |
| `data.status` | string |  |
| `data.task_id` | string |  |
| `data.task_type` | string |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Skyreels API, this operation is `GET /api/v1/task/:task_id` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-skyreels-task.md) for the provider-specific parameters and requirements.

