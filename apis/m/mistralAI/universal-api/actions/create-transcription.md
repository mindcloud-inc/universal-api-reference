# Mistral AI: Create Transcription

Creates an audio transcription in Mistral AI.

```
POST https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/create-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/create-transcription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/create-transcription', {
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
| `model` | string | yes | ID of the transcription model to use. |
| `file` | file | no | Audio file object to transcribe. |
| `fileUrl` | string | no | URL of the audio file to transcribe. |
| `fileId` | string | no | ID of an uploaded file to transcribe. |
| `language` | string | no | Language hint for the audio. |
| `temperature` | number | no | Sampling temperature for transcription decoding. |
| `stream` | boolean | no | Whether to stream partial transcription progress. |
| `diarize` | boolean | no | Whether to enable speaker diarization. |
| `contextBias[]` | array<string> | no | Optional context-bias phrases. |
| `timestampGranularities[]` | array<string> | no | Timestamp granularities to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "language": "string",
      "model": "string",
      "segments": [
        {}
      ],
      "text": "string",
      "type": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `language` | string |  |
| `model` | string |  |
| `segments` | array<object> |  |
| `text` | string |  |
| `type` | string |  |
| `usage` | object |  |

## Native endpoint

Through the native Mistral AI API, this operation is `POST /v1/audio/transcriptions` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcription.md) for the provider-specific parameters and requirements.

