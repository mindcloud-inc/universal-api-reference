# Voicemaker: Generate TTS

Creates synthesized speech from text in Voicemaker.

```
POST https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/generate-tts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voicemaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/generate-tts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceId": "string",
  "languageCode": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/generate-tts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceId": "string",
    "languageCode": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voiceId` | string | yes | Voice ID to synthesize with, for example ai3-Jony. |
| `languageCode` | string | yes | Language code for the selected voice, for example en-US. |
| `text` | string | yes | Text or SSML content to convert to speech. |
| `outputFormat` | string | no | Audio format such as mp3, wav, ogg, opus, aac, ulaw, or alaw. |
| `sampleRate` | number | no | Sample rate, for example 22050, 24000, 44100, or 48000. |
| `masterVolume` | number | no | Volume adjustment from -20 to 20. |
| `masterSpeed` | number | no | Speed adjustment from -100 to 100. |
| `masterPitch` | number | no | Pitch adjustment from -100 to 100. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "path": "string",
      "remainChars": 1,
      "remainKeyChars": 1,
      "success": true,
      "usedChars": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `path` | string |  |
| `remainChars` | number |  |
| `remainKeyChars` | number |  |
| `success` | boolean |  |
| `usedChars` | number |  |

## Native endpoint

Through the native Voicemaker API, this operation is `POST api/v1/voice/convert` (base URL `https://developer.voicemaker.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-tts.md) for the provider-specific parameters and requirements.

