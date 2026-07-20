# LMNT: Generate Speech (Detailed)

Creates timestamped speech output from text in LMNT.

```
POST https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/generate-speech-detailed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LMNT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/generate-speech-detailed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "voice": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/generate-speech-detailed', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "voice": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | no | Optional output audio format such as mp3, wav, webm, ulaw, pcm_s16le, pcm_f32le, or aac. |
| `language` | string | no | Optional ISO 639-1 language code. Defaults to auto-detection. |
| `returnDurations` | boolean | no | When true, LMNT includes word-level timing data in the response. |
| `sampleRate` | number | no | Optional output sample rate in Hz. |
| `seed` | number | no | Optional seed to reproduce a take. |
| `text` | string | yes | The text to synthesize. LMNT documents a maximum of 5000 characters per request. |
| `voice` | string | yes | The voice id to use for synthesis. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audio": "string",
      "durations": [
        {}
      ],
      "seed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audio` | string |  |
| `durations` | array<object> |  |
| `seed` | number |  |

## Native endpoint

Through the native LMNT API, this operation is `POST /v1/ai/speech` (base URL `https://api.lmnt.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-speech-detailed.md) for the provider-specific parameters and requirements.

