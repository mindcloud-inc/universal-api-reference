# PiAPI/Qwen: Create Image Edit Task

Creates an image edit task in PiAPI/Qwen.

```
POST https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/create-image-edit-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Qwen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/create-image-edit-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.image1": "https://example.com/image1.png",
  "input.prompt": "Describe the edit you want"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/create-image-edit-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.image1": "https://example.com/image1.png",
    "input.prompt": "Describe the edit you want"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.image1` | string | yes | Example: `https://example.com/image1.png`. |
| `input.prompt` | string | yes | Example: `Describe the edit you want`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.image2` | string | no | Example: `https://example.com/image2.png`. |
| `input.image3` | string | no | Example: `https://example.com/image3.png`. |
| `input.negative_prompt` | string | no | Example: `What to avoid`. |
| `input.seed` | number | no | Example: `-1`. |
| `input.steps` | number | no | Example: `8`. |
| `input.flow_shift` | number | no | Example: `3`. |
| `config.webhook_config.endpoint` | string | no | Example: `https://example.com/webhook`. |
| `config.webhook_config.secret` | string | no | Example: `optional-secret`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "model": "string",
        "status": "string",
        "task_id": "string",
        "task_type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | HTTP-style success code returned by PiAPI create-task response. |
| `data.model` | string | Model used for the task. |
| `data.status` | string | Current task status immediately after creation. |
| `data.task_id` | string | Created PiAPI task identifier. |
| `data.task_type` | string | PiAPI task type for the created task. |

## Native endpoint

Through the native PiAPI/Qwen API, this operation is `POST /task` (base URL `https://api.piapi.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image-edit-task.md) for the provider-specific parameters and requirements.

