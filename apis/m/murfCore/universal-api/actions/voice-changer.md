# Murf Core: Voice Changer

Converts audio to another voice with Murf Core.

```
POST https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/voice-changer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Murf Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/voice-changer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/voice-changer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voiceId` | string | yes | Target Murf voice ID for the converted audio. |
| `file` | file | no | Audio file to convert. |
| `fileUrl` | string | no | Public URL for the source audio file. |
| `format` | string | no | Output audio format. |
| `encodeOutputAsBase64` | boolean | no | Return the generated audio as base64 in the response. |
| `channelType` | string | no | Output channel type. |
| `sampleRate` | number | no | Output sample rate in hertz. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audio_file": "string",
      "audio_length_in_seconds": 1,
      "encoded_audio": "string",
      "remaining_character_count": 1,
      "warning": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audio_file` | string | URL for the converted audio file. |
| `audio_length_in_seconds` | number | Length of the converted audio in seconds. |
| `encoded_audio` | string | Base64-encoded converted audio when requested. |
| `remaining_character_count` | number | Remaining characters available after the conversion. |
| `warning` | string | Optional warning returned by Murf. |

## Native endpoint

Through the native Murf Core API, this operation is `POST /v1/voice-changer/convert` (base URL `https://api.murf.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/voice-changer.md) for the provider-specific parameters and requirements.

