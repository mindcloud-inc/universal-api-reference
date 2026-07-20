# ElevenLabs: Create Transcript

Creates a transcript from audio or video in ElevenLabs.

```
POST https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/create-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ElevenLabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/create-transcript" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloudStorageUrl": "https://example.com",
  "modelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/create-transcript', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloudStorageUrl": "https://example.com",
    "modelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cloudStorageUrl` | string | yes | A public audio file URL for transcription. |
| `modelId` | string | yes | The speech-to-text model identifier. |
| `languageCode` | string | no |  |
| `tagAudioEvents` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ElevenLabs API returns.

## Native endpoint

Through the native ElevenLabs API, this operation is `POST /speech-to-text` (base URL `https://api.elevenlabs.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcript.md) for the provider-specific parameters and requirements.

