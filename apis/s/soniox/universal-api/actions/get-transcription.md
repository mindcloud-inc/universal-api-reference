# Soniox: Get transcription

Retrieves a transcription from Soniox.

```
GET https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Soniox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-transcription?connectionId=$CONNECTION_ID&transcriptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/soniox/latest/actions/get-transcription?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transcriptionId` | string | yes | Unique identifier of the transcription. |

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

Through the native Soniox API, this operation is `GET /transcriptions/:transcription_id` (base URL `https://api.soniox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcription.md) for the provider-specific parameters and requirements.

