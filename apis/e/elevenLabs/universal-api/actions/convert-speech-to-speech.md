# ElevenLabs: Convert Speech To Speech

Transforms audio from one voice to another in ElevenLabs.

```
POST https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/convert-speech-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ElevenLabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/convert-speech-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceId": "string",
  "audio": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/convert-speech-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceId": "string",
    "audio": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voiceId` | string | yes | ID of the target voice. |
| `audio` | file | yes | Audio file or public file URL to convert. |
| `outputFormat` | string | no | Generated audio output format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelId` | string | no | Speech-to-speech model to use. |
| `voiceSettings` | string | no | JSON-encoded voice settings override string. |
| `seed` | number | no | Deterministic sampling seed. |
| `removeBackgroundNoise` | boolean | no | Whether to remove background noise before conversion. |
| `fileFormat` | string | no | Input audio format. |
| `enableLogging` | boolean | no | Whether to retain history and request stitching. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ElevenLabs API returns.

## Native endpoint

Through the native ElevenLabs API, this operation is `POST /speech-to-speech/:voice_id` (base URL `https://api.elevenlabs.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-speech-to-speech.md) for the provider-specific parameters and requirements.

