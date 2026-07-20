# Murf Core: Synthesize Speech

Synthesizes speech from text in Murf Core.

```
POST https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/synthesize-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Murf Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/synthesize-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "voiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/synthesize-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "voiceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | The text to synthesize into speech. |
| `voiceId` | string | yes | Voice identifier from the List Voices action. |
| `locale` | string | no | Optional target locale for multi-native generation. |
| `format` | string | no | Optional output format such as WAV, MP3, or FLAC. |
| `encodeAsBase64` | boolean | no | Return audio inline as base64 instead of a hosted URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioFile": "string",
      "audioLengthInSeconds": 1,
      "consumedCharacterCount": 1,
      "encodedAudio": "string",
      "remainingCharacterCount": 1,
      "warning": "string",
      "wordDurations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioFile` | string | URL for the generated audio file. |
| `audioLengthInSeconds` | number | Length of the generated audio in seconds. |
| `consumedCharacterCount` | number | Characters consumed in the current billing cycle. |
| `encodedAudio` | string | Base64-encoded audio when requested. |
| `remainingCharacterCount` | number | Remaining characters available for synthesis in the current billing cycle. |
| `warning` | string | Optional warning returned by Murf. |
| `wordDurations` | array<object> | Per-word timing metadata for the generated speech. |

## Native endpoint

Through the native Murf Core API, this operation is `POST /v1/speech/generate` (base URL `https://api.murf.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/synthesize-speech.md) for the provider-specific parameters and requirements.

