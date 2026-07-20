# Mihu AI: Create a New Transcription Request



```
POST https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/create-a-new-transcription-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/create-a-new-transcription-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/create-a-new-transcription-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `coachingAgentUuid` | string | no |  |
| `customerEmail` | string | no |  |
| `customerPhone` | string | no |  |
| `email` | string | no |  |
| `possibleConversation` | string | no |  |
| `possibleLanguage` | string | no |  |
| `qaAgentUuid` | string | no |  |
| `referenceId` | string | no |  |
| `voiceUrl` | string | no |  |
| `webhookHeaderToken` | string | no |  |
| `webhookUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "coachingAgentUuid": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "errorMessage": "string",
      "possibleLanguage": "string",
      "processedAt": "2026-05-07T12:00:00.000Z",
      "qaAgentUuid": "string",
      "referenceId": "string",
      "s3FilePath": "string",
      "s3FileUrl": "https://example.com",
      "status": "string",
      "transcriptionResult": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coachingAgentUuid` | string |  |
| `createdAt` | date |  |
| `errorMessage` | string |  |
| `possibleLanguage` | string |  |
| `processedAt` | date |  |
| `qaAgentUuid` | string |  |
| `referenceId` | string |  |
| `s3FilePath` | string |  |
| `s3FileUrl` | string |  |
| `status` | string |  |
| `transcriptionResult` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mihu AI API, this operation is `POST /api/v1/transcriptions` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-transcription-request.md) for the provider-specific parameters and requirements.

