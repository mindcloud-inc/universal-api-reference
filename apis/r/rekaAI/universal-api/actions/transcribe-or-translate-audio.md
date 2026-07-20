# Reka AI: Transcribe or Translate Audio

Creates an audio transcription or translation in Reka AI.

```
POST https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/transcribe-or-translate-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/transcribe-or-translate-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audio_url": "https://example.com",
  "sampling_rate": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/transcribe-or-translate-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audio_url": "https://example.com",
    "sampling_rate": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audio_url` | string | yes | Audio file URL or data URI |
| `sampling_rate` | number | yes | Audio sampling rate in Hz |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "language": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number | Audio duration. |
| `language` | string | Detected language. |
| `text` | string | Transcribed or translated text. |

## Native endpoint

Through the native Reka AI API, this operation is `POST /v1/transcription_or_translation` (base URL `https://api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transcribe-or-translate-audio.md) for the provider-specific parameters and requirements.

