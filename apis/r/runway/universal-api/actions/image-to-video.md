# Runway: Image To Video

Creates a video generation task from an image in Runway.

```
POST https://connect.mindcloud.co/v1/universal/runway/latest/actions/image-to-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/image-to-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "gen4.5",
  "promptImage": "string",
  "promptText": "string",
  "ratio": "string",
  "duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/image-to-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "gen4.5",
    "promptImage": "string",
    "promptText": "string",
    "ratio": "string",
    "duration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Generation model, such as gen4.5, gen4_turbo, gen3a_turbo, veo3.1, veo3.1_fast, or veo3. Default: `gen4.5`. |
| `promptImage` | string | yes | HTTPS URL, Runway URI, or data URI for the source image. |
| `promptText` | string | yes | Detailed text prompt for the video generation. |
| `ratio` | string | yes | Aspect ratio for the output video. Example: 1280:720. |
| `duration` | number | yes | Output duration in seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "error": "string",
      "id": "string",
      "progress": 1,
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `error` | string |  |
| `id` | string |  |
| `progress` | number |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Runway API, this operation is `POST /v1/image_to_video` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/image-to-video.md) for the provider-specific parameters and requirements.

