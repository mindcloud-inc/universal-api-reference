# AssemblyAI: Search Transcript Words

Finds keywords in an AssemblyAI transcript.

```
GET https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/search-transcript-words
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssemblyAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/search-transcript-words?connectionId=$CONNECTION_ID&transcriptId=string&words=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptId": "string",
  "words": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/search-transcript-words?${params}`, {
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
| `transcriptId` | string | yes | The transcript ID to search. |
| `words` | string | yes | One or more keywords to search for in the transcript. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "matches": [
        [
          {}
        ]
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `matches[]` | array<object> |  |
| `matches[].count` | number |  |
| `matches[].indexes[]` | array<number> |  |
| `matches[].text` | string |  |
| `matches[].timestamps[]` | array<object> |  |
| `matches[].timestamps[].value0` | number |  |
| `matches[].timestamps[].value1` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native AssemblyAI API, this operation is `GET /v2/transcript/:transcript_id/word-search` (base URL `https://api.assemblyai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-transcript-words.md) for the provider-specific parameters and requirements.

