# PiAPI/Qwen: Get Task

Retrieves task status details from PiAPI/Qwen.

```
GET https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Qwen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/get-task?connectionId=$CONNECTION_ID&task_id=task-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "task_id": "task-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/get-task?${params}`, {
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
| `task_id` | string | yes | Example: `task-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "model": "string",
        "output": {
          "image_url": "https://example.com"
        },
        "status": "string",
        "task_id": "string",
        "task_type": "string"
      },
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.model` | string | Model used for the task. |
| `data.output.image_url` | string | Generated image URL when the task output is available. |
| `data.status` | string | Current PiAPI task status. |
| `data.task_id` | string | PiAPI task identifier. |
| `data.task_type` | string | PiAPI task type for the task. |
| `timestamp` | number | Unix timestamp for the task lookup response. |

## Native endpoint

Through the native PiAPI/Qwen API, this operation is `GET /task/{task_id}` (base URL `https://api.piapi.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

