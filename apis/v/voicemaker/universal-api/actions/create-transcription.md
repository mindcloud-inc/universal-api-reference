# Voicemaker: Create Transcription

Creates a transcription from audio in Voicemaker.

```
POST https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/create-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voicemaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/create-transcription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/create-transcription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Audio file to transcribe. |
| `model` | string | no | Transcription model, for example stt-flagship-v1. |
| `language` | string | no | Language code or auto for auto-detection. |
| `responseFormat` | string | no | Desired transcription response format. |
| `includeSubtitle` | boolean | no | Whether to include subtitle output. |
| `tagAudioEvents` | boolean | no | Whether to tag audio events in the transcription. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "isProcessing": true,
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
| `data` | object |  |
| `isProcessing` | boolean |  |
| `remainChars` | number |  |
| `remainKeyChars` | number |  |
| `success` | boolean |  |
| `usedChars` | number |  |

## Native endpoint

Through the native Voicemaker API, this operation is `POST api/v1/speech-to-text` (base URL `https://developer.voicemaker.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcription.md) for the provider-specific parameters and requirements.

