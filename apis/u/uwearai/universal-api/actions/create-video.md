# Uwear.ai: Create Video

Creates a video generation in Uwear.ai.

```
POST https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/create-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uwear.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/create-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/create-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `duration` | number | no | Optional video duration in seconds. |
| `generation_result_id` | number | no | Generation result ID to animate. |
| `image_url` | string | no | Direct image URL to animate. |
| `model_name` | string | no | Optional Uwear video model name. |
| `prompt` | string | no | Optional motion prompt for the video. |
| `resolution` | string | no | Optional output resolution. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "generation_id": 1,
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `generation_id` | number |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Uwear.ai API, this operation is `POST /api/v1/generation-video` (base URL `https://api.uwear.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video.md) for the provider-specific parameters and requirements.

