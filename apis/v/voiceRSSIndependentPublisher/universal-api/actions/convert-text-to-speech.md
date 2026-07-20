# VoiceRSS (Independent Publisher): Convert Text to Speech

Creates speech audio from text in VoiceRSS.

```
POST https://connect.mindcloud.co/v1/universal/voiceRSSIndependentPublisher/latest/actions/convert-text-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceRSS (Independent Publisher) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceRSSIndependentPublisher/latest/actions/convert-text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "language": "en-us",
  "source_text": "Hello, world!"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceRSSIndependentPublisher/latest/actions/convert-text-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "language": "en-us",
    "source_text": "Hello, world!"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | yes | Text language code, such as `en-us`. Example: `en-us`. |
| `source_text` | string | yes | Text to convert to speech. VoiceRSS limits this to 100KB. Example: `Hello, world!`. |
| `voice` | string | no | Optional VoiceRSS voice name. Default depends on the selected language. Example: `Linda`. |
| `rate` | number | no | Speech rate from -10 through 10. Default is 0. Default: `0`. |
| `codec` | list<string> | no | Audio codec. Defaults to WAV when omitted. One of: `0`, `1`, `2`, `3`, `4`. Default: `MP3`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | no | Audio format. Defaults to 8khz_8bit_mono when omitted. Default: `16khz_16bit_stereo`. |
| `ssml` | boolean | no | Whether source text uses SSML format. Default: `false`. |
| `base64_output` | boolean | no | Return audio as a Base64 string instead of binary audio data. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioContent": "string",
      "contentLength": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioContent` | string | Base64-encoded audio content when Base64 Output is enabled, or the raw audio text payload returned by VoiceRSS. |
| `contentLength` | number | Length of the returned audio content string after mapper normalization. |

## Native endpoint

Through the native VoiceRSS (Independent Publisher) API, this operation is `GET /` (base URL `https://api.voicerss.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-text-to-speech.md) for the provider-specific parameters and requirements.

