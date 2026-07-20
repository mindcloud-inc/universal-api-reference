# PiAPI/Skyreels: Create Skyreels Task

Creates a new Skyreels task in PiAPI.

```
POST https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/create-skyreels-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Skyreels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/create-skyreels-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "FPS-24, gentle camera move over a portrait photo",
  "input.image": "https://example.com/source-image.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/create-skyreels-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "FPS-24, gentle camera move over a portrait photo",
    "input.image": "https://example.com/source-image.png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.prompt` | string | yes | Prompt describing the motion or video to generate. Example: `FPS-24, gentle camera move over a portrait photo`. |
| `input.image` | string | yes | Source image URL for the Skyreels img2video task. Example: `https://example.com/source-image.png`. |
| `input.aspectRatio` | list | no | Optional output aspect ratio. One of: `0`, `1`, `2`. Default: `16:9`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.negativePrompt` | string | no | Optional prompt describing what to avoid. Example: `chaotic, distortion, morphing`. |
| `input.guidanceScale` | number | no | Optional guidance scale value. Default: `3.5`. Example: `3.5`. |

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
| `data.status` | string |  |
| `data.task_id` | string |  |
| `data.task_type` | string |  |
| `message` | string |  |

## Native endpoint

Through the native PiAPI/Skyreels API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-skyreels-task.md) for the provider-specific parameters and requirements.

