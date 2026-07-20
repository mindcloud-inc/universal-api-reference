# PiAPI/Qwen: Create Text to Image Task

Creates a text-to-image task in PiAPI/Qwen.

```
POST https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/create-text-to-image-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Qwen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/create-text-to-image-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "A detailed image prompt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/create-text-to-image-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "A detailed image prompt"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.prompt` | string | yes | Example: `A detailed image prompt`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.seed` | number | no | Example: `-1`. |
| `input.steps` | number | no | Example: `16`. |
| `input.width` | number | no | Example: `1024`. |
| `input.height` | number | no | Example: `1024`. |
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

Through the native PiAPI/Qwen API, this operation is `POST /task` (base URL `https://api.piapi.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-to-image-task.md) for the provider-specific parameters and requirements.

