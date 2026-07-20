# PiAPI/Sora: Create Sora2 Text to Video Task



```
POST https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/create-sora2-text-to-video-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Sora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/create-sora2-text-to-video-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "A cinematic drone shot over a neon city at dusk"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/create-sora2-text-to-video-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "A cinematic drone shot over a neon city at dusk"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.prompt` | string | yes | Text prompt for the Sora2 video. Example: `A cinematic drone shot over a neon city at dusk`. |
| `input.aspectRatio` | string | no | Aspect ratio sent to PiAPI. Example: `16:9`. |
| `input.duration` | number | no | Video duration in seconds. Example: `4`. |

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
| `data.status` | string |  |
| `data.task_id` | string |  |
| `data.task_type` | string |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Sora API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sora2-text-to-video-task.md) for the provider-specific parameters and requirements.

