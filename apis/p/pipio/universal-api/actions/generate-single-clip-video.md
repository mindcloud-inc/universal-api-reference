# Pipio: Generate Single Clip Video

Creates a single-clip video in Pipio.

```
POST https://connect.mindcloud.co/v1/universal/pipio/latest/actions/generate-single-clip-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipio/latest/actions/generate-single-clip-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actorId": "7528735effb7cde8cd5474dc110905c2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipio/latest/actions/generate-single-clip-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actorId": "7528735effb7cde8cd5474dc110905c2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actorId` | string | yes | The unique identifier for your digital actor. Default: `7528735effb7cde8cd5474dc110905c2`. Example: `7528735effb7cde8cd5474dc110905c2`. |
| `voiceId` | string | no | The unique identifier for your voice. Only voiceId or language may be sent per request. Default: `b2c11ebef1e47591f75bceef56635435`. Example: `b2c11ebef1e47591f75bceef56635435`. |
| `script` | string | no | Text script to generate a performance from your digital actor. Default: `Hello world`. Example: `Hello world`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | no | Language code to apply to the selected avatar. Only language or voiceId may be sent per request. Example: `en-US`. |
| `audioUrl` | string | no | URL to an audio file that will be used instead of script-based text to speech. Example: `https://example.com/audio.mp3`. |
| `fps` | number | no | Frame rate of the video, either 30 or 60. Default: `60`. Example: `60`. |
| `transparent` | boolean | no | Whether to render the video with a transparent background. Default: `false`. |
| `callbackUrl` | string | no | Location the server will send the response to. Example: `https://example.com/webhook`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "actorId": "string",
      "aspectRatio": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "creditCost": 1,
      "fps": 1,
      "id": "string",
      "language": "string",
      "processingStatus": "string",
      "script": "string",
      "status": "string",
      "transparent": true,
      "voiceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Account id that owns the generated video. |
| `actorId` | string | Actor id used for the generation request. |
| `aspectRatio` | number | Aspect ratio of the generated video. |
| `createdDate` | date | Creation timestamp reported by Pipio. |
| `creditCost` | number | Credit cost reported by Pipio. |
| `fps` | number | Frame rate for the generated video. |
| `id` | string | Generated video id. |
| `language` | string | Resolved language for the generated video. |
| `processingStatus` | string | Detailed processing status. |
| `script` | string | Script sent for generation. |
| `status` | string | Generation status. |
| `transparent` | boolean | Whether transparent background rendering is enabled. |
| `voiceId` | string | Voice id used for the generation request. |

## Native endpoint

Through the native Pipio API, this operation is `POST https://generate.pipio.ai/single-clip` (base URL `https://avatar.pipio.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-single-clip-video.md) for the provider-specific parameters and requirements.

