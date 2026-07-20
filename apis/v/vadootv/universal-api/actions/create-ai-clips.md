# Vadootv: Create AI clips

Creates an AI clips job in Vadootv.

```
POST https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/create-ai-clips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vadootv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/create-ai-clips" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video_url": "https://example.com/video.mp4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/create-ai-clips', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "video_url": "https://example.com/video.mp4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `video_url` | string | yes | URL of the source long-form video. Example: `https://example.com/video.mp4`. |
| `num_highlights` | number | no | Number of viral clips to extract. Default: `3`. Example: `3`. |
| `aspect_ratio` | list<string> | no | Target aspect ratio for generated clips. One of: `16:9`, `1:1`, `9:16`. Default: `9:16`. |
| `return_coordinates_only` | boolean | no | Return bounding box coordinates without rendering the video. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request_id` | string | Request ID for the generated clips job. |

## Native endpoint

Through the native Vadootv API, this operation is `POST /api/create_ai_clips` (base URL `https://aiapi.vadoo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ai-clips.md) for the provider-specific parameters and requirements.

