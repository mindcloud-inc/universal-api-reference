# PiAPI/Luma (unofficial): Create Luma Task

Creates a new Luma task in PiAPI.

```
POST https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/create-luma-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Luma (unofficial) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/create-luma-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/create-luma-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.prompt` | string | yes | Prompt describing the video to generate. |
| `input.duration` | number | no | Output video duration in seconds. Default: `5`. |
| `input.aspectRatio` | string | no | Output aspect ratio for the generated video. Default: `16:9`. |
| `input.startImage` | string | no | Optional starting image URL for image-to-video generation. |
| `input.endImage` | string | no | Optional ending image URL for keyframe-guided generation. |
| `input.loop` | boolean | no | Whether the generated clip should loop. Default: `false`. |

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
| `code` | number | PiAPI status code. |
| `data` | object | Task payload returned on create, including failed task attempts. |
| `data.config` | object | Task configuration. |
| `data.detail` | object | Provider detail payload when present. |
| `data.error` | object | Provider error payload when the task fails. |
| `data.input` | object | Submitted generation input. |
| `data.logs` | array<string> | Provider log messages. |
| `data.meta` | object | Provider metadata including timestamps and usage. |
| `data.model` | string | Provider model family. |
| `data.output` | object | Generated output when available. |
| `data.status` | string | Current task status. |
| `data.task_id` | string | PiAPI task identifier. |
| `data.task_type` | string | PiAPI task type. |
| `message` | string | PiAPI status message. |

## Native endpoint

Through the native PiAPI/Luma (unofficial) API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-luma-task.md) for the provider-specific parameters and requirements.

