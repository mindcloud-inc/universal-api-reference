# PiAPI/Toolkit: Image Upscale (Super Resolution) API

Creates an image-upscale task in PiAPI/Toolkit.

```
POST https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/image-upscale-super-resolution
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Toolkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/image-upscale-super-resolution" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://example.com",
  "scale": "2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIToolkit/latest/actions/image-upscale-super-resolution', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://example.com",
    "scale": "2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes | Doc-backed PiAPI field for Image Upscale (Super Resolution) API. |
| `scale` | number | yes | Doc-backed PiAPI field for Image Upscale (Super Resolution) API. Default: `2`. |
| `faceEnhance` | boolean | no | Doc-backed PiAPI field for Image Upscale (Super Resolution) API. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
        "face_enhance": true,
        "image": "string",
        "scale": 1
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config.service_mode` | string |  |
| `config.webhook_config.endpoint` | string |  |
| `config.webhook_config.secret` | string |  |
| `error.code` | number |  |
| `error.message` | string |  |
| `error.raw_message` | string |  |
| `input.face_enhance` | boolean |  |
| `input.image` | string |  |
| `input.scale` | number |  |
| `meta.created_at` | date |  |
| `meta.ended_at` | date |  |
| `meta.is_using_private_pool` | boolean |  |
| `meta.started_at` | date |  |
| `meta.usage.consume` | number |  |
| `meta.usage.frozen` | number |  |
| `meta.usage.type` | string |  |
| `model` | string |  |
| `status` | string |  |
| `task_id` | string |  |
| `task_type` | string |  |

## Native endpoint

Through the native PiAPI/Toolkit API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/image-upscale-super-resolution.md) for the provider-specific parameters and requirements.

