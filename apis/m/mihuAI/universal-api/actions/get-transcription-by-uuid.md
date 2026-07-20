# Mihu AI: Get Transcription by UUID



```
GET https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-transcription-by-uuid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-transcription-by-uuid?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-transcription-by-uuid?${params}`, {
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
| `uuid` | string | yes |  |

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

Through the native Mihu AI API, this operation is `GET /api/v1/transcriptions/:uuid` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcription-by-uuid.md) for the provider-specific parameters and requirements.

