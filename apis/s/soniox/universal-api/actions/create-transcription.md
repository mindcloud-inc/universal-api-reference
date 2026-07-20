# Soniox: Create transcription

Creates a new transcription in Soniox.

```
POST https://connect.mindcloud.co/v1/universal/soniox/latest/actions/create-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soniox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/soniox/latest/actions/create-transcription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/soniox/latest/actions/create-transcription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Speech-to-text model to use for the transcription. |
| `audioUrl` | string | no | Public URL of the audio file to transcribe. |
| `fileId` | string | no | Uploaded file ID to transcribe instead of an audio URL. |
| `languageHints[]` | array<string> | no | Expected languages in the audio. |
| `languageHintsStrict` | boolean | no | Rely more heavily on the provided language hints. |
| `enableSpeakerDiarization` | boolean | no | Identify and separate speakers in the transcription output. |
| `enableLanguageIdentification` | boolean | no | Detect the language for each part of the transcription. |
| `translation.type` | string | no | Translation mode for the transcription. |
| `translation.targetLanguage` | string | no | Target language for one-way translation. |
| `translation.languageA` | string | no | First language for two-way translation. |
| `translation.languageB` | string | no | Second language for two-way translation. |
| `context` | string | no | Additional context to improve transcription accuracy. |
| `webhookUrl` | string | no | Webhook URL for completion or failure notifications. |
| `webhookAuthHeaderName` | string | no | Name of the auth header sent with webhook notifications. |
| `webhookAuthHeaderValue` | string | no | Value of the auth header sent with webhook notifications. |
| `clientReferenceId` | string | no | Optional tracking identifier for your system. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioDurationMs": 1,
      "audioUrl": "https://example.com",
      "clientReferenceId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enableAudioEventDetection": true,
      "enableLanguageIdentification": true,
      "enableSpeakerDiarization": true,
      "errorMessage": "string",
      "errorType": "string",
      "fileId": "string",
      "filename": "Ava Chen",
      "id": "string",
      "languageHints": [
        "string"
      ],
      "model": "string",
      "status": "string",
      "webhookAuthHeaderName": "Ava Chen",
      "webhookAuthHeaderValue": "string",
      "webhookStatusCode": 1,
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioDurationMs` | number | Audio duration in milliseconds. |
| `audioUrl` | string | Audio URL used for the transcription. |
| `clientReferenceId` | string | Optional client tracking identifier. |
| `createdAt` | date | Creation timestamp. |
| `enableAudioEventDetection` | boolean | Whether audio event detection is enabled. |
| `enableLanguageIdentification` | boolean | Whether language identification is enabled. |
| `enableSpeakerDiarization` | boolean | Whether speaker diarization is enabled. |
| `errorMessage` | string | Error message when the transcription fails. |
| `errorType` | string | Error type when the transcription fails. |
| `fileId` | string | Uploaded file ID used for the transcription. |
| `filename` | string | Resolved audio filename. |
| `id` | string | Unique transcription identifier. |
| `languageHints` | array<string> | Requested language hints. |
| `model` | string | Transcription model ID. |
| `status` | string | Current transcription status. |
| `webhookAuthHeaderName` | string | Webhook auth header name. |
| `webhookAuthHeaderValue` | string | Webhook auth header value. |
| `webhookStatusCode` | number | Most recent webhook delivery status code. |
| `webhookUrl` | string | Webhook target URL. |

## Native endpoint

Through the native Soniox API, this operation is `POST /transcriptions` (base URL `https://api.soniox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcription.md) for the provider-specific parameters and requirements.

