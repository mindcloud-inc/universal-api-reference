# AssemblyAI: Get Transcript Paragraphs

Retrieves paragraph segments from an AssemblyAI transcript.

```
GET https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/get-transcript-paragraphs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssemblyAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/get-transcript-paragraphs?connectionId=$CONNECTION_ID&transcriptId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/get-transcript-paragraphs?${params}`, {
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
| `transcriptId` | string | yes | The transcript ID to retrieve paragraphs for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioDuration": 1,
      "confidence": 1,
      "id": "string",
      "paragraphs": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioDuration` | number |  |
| `confidence` | number |  |
| `id` | string |  |
| `paragraphs[]` | array<object> |  |
| `paragraphs[].confidence` | number |  |
| `paragraphs[].end` | number |  |
| `paragraphs[].start` | number |  |
| `paragraphs[].text` | string |  |
| `paragraphs[].words[]` | array<object> |  |
| `paragraphs[].words[].confidence` | number |  |
| `paragraphs[].words[].end` | number |  |
| `paragraphs[].words[].start` | number |  |
| `paragraphs[].words[].text` | string |  |

## Native endpoint

Through the native AssemblyAI API, this operation is `GET /v2/transcript/:transcript_id/paragraphs` (base URL `https://api.assemblyai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcript-paragraphs.md) for the provider-specific parameters and requirements.

