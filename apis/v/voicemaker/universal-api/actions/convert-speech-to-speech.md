# Voicemaker: Convert Speech to Speech

Creates converted speech from uploaded audio in Voicemaker.

```
POST https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/convert-speech-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voicemaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/convert-speech-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "voiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/convert-speech-to-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "voiceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Source audio file to re-voice. |
| `voiceId` | string | yes | Target ProPlus or cloned voice ID. |
| `outputFormat` | string | no | Audio output format. |
| `sampleRate` | number | no | Output sample rate. |
| `responseType` | string | no | Response mode for generated audio. |
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

Through the native Voicemaker API, this operation is `POST api/v1/speech-to-speech` (base URL `https://developer.voicemaker.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-speech-to-speech.md) for the provider-specific parameters and requirements.

