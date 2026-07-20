# Datamuse: Get Word Metadata

Retrieves Datamuse metadata for a word by exact spelling.

```
GET https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/get-word-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datamuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/get-word-metadata?connectionId=$CONNECTION_ID&word=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "word": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/get-word-metadata?${params}`, {
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
| `word` | string | yes | Word to look up metadata for. |
| `metadataFlags` | string | no | Metadata flags to include. Datamuse supports d, p, s, r, and f. Default: `dpsrf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defHeadword": "string",
      "defs": [
        "string"
      ],
      "numSyllables": 1,
      "score": 1,
      "tags": [
        "string"
      ],
      "word": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defHeadword` | string | Headword for a returned definition entry. |
| `defs` | array<string> | Definitions returned by Datamuse. |
| `numSyllables` | number | Syllable count. |
| `score` | number | Datamuse ranking score. |
| `tags` | array<string> | Part-of-speech, pronunciation, frequency, and query metadata tags. |
| `word` | string | Matched word. |

## Native endpoint

Through the native Datamuse API, this operation is `GET /words` (base URL `https://api.datamuse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-word-metadata.md) for the provider-specific parameters and requirements.

