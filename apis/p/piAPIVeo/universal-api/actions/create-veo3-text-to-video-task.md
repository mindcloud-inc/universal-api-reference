# PiAPI/Veo: Create Veo3 Text to Video Task

Creates a Veo 3 text-to-video task in PiAPI/Veo.

```
POST https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/create-veo3-text-to-video-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Veo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/create-veo3-text-to-video-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "string",
  "taskType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/create-veo3-text-to-video-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "string",
    "taskType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.prompt` | string | yes |  |
| `input.negativePrompt` | string | no |  |
| `taskType` | string | yes | Use veo3-video or veo3-video-fast. |
| `input.aspectRatio` | string | no |  |
| `input.duration` | string | no |  |
| `input.resolution` | string | no |  |
| `input.generateAudio` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "status": "string",
        "task_id": "string"
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
| `data` | object |  |
| `data.status` | string |  |
| `data.task_id` | string |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Veo API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-veo3-text-to-video-task.md) for the provider-specific parameters and requirements.

