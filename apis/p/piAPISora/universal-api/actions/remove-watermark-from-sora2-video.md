# PiAPI/Sora: Remove Watermark from Sora2 Video



```
POST https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/remove-watermark-from-sora2-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PiAPI/Sora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/remove-watermark-from-sora2-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.videoUrl": "https://example.com/sora-watermarked.mp4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/remove-watermark-from-sora2-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.videoUrl": "https://example.com/sora-watermarked.mp4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input.videoUrl` | string | yes | URL of the Sora video that still has a watermark. Example: `https://example.com/sora-watermarked.mp4`. |

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

Through the native PiAPI/Sora API, this operation is `POST /api/v1/task` (base URL `https://api.piapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-watermark-from-sora2-video.md) for the provider-specific parameters and requirements.

