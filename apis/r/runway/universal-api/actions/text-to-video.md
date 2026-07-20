# Runway: Text To Video

Creates a video generation task from text in Runway.

```
POST https://connect.mindcloud.co/v1/universal/runway/latest/actions/text-to-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/text-to-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "duration": "5",
  "model": "gen4.5",
  "promptText": "string",
  "ratio": "1280:720"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/text-to-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "duration": "5",
    "model": "gen4.5",
    "promptText": "string",
    "ratio": "1280:720"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `duration` | number | yes | Requested output duration in seconds, between 2 and 10. Default: `5`. |
| `model` | string | yes | Generation model, such as gen4.5, veo3.1, veo3.1_fast, or veo3. Default: `gen4.5`. |
| `promptText` | string | yes | Detailed text prompt for the video generation. |
| `ratio` | string | yes | Output video ratio, such as 1280:720 or 720:1280. Default: `1280:720`. |

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

Through the native Runway API, this operation is `POST /v1/text_to_video` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/text-to-video.md) for the provider-specific parameters and requirements.

