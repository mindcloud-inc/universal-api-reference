# AssemblyAI: Get Redacted Audio

Retrieves redacted audio details from an AssemblyAI transcript.

```
GET https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/get-redacted-audio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssemblyAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/get-redacted-audio?connectionId=$CONNECTION_ID&transcriptId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/get-redacted-audio?${params}`, {
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
| `transcriptId` | string | yes | ID of the transcript. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "redactedAudioUrl": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `redactedAudioUrl` | string |  |
| `status` | string |  |

## Native endpoint

Through the native AssemblyAI API, this operation is `GET /v2/transcript/:transcript_id/redacted-audio` (base URL `https://api.assemblyai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-redacted-audio.md) for the provider-specific parameters and requirements.

