# Grok: Generate Video

Creates a video generation request in Grok.

```
POST https://connect.mindcloud.co/v1/universal/grok/latest/actions/generate-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grok/latest/actions/generate-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/generate-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | xAI video generation model. |
| `prompt` | string | yes | Text prompt describing the video to generate. |
| `image` | object | no | Optional source image for image-to-video generation. |
| `duration` | number | no | Desired video duration in seconds. |
| `aspectRatio` | string | no | Desired output aspect ratio. |
| `resolution` | string | no | Desired output resolution. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string | Asynchronous video generation request identifier. |

## Native endpoint

Through the native Grok API, this operation is `POST /v1/videos/generations` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-video.md) for the provider-specific parameters and requirements.

