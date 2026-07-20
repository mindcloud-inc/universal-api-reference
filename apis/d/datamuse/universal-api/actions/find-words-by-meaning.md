# Datamuse: Find Words By Meaning

Finds words in Datamuse by related meaning.

```
GET https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-words-by-meaning
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datamuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-words-by-meaning?connectionId=$CONNECTION_ID&meaning=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meaning": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-words-by-meaning?${params}`, {
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
| `meaning` | string | yes | Word or phrase that the results should have a similar meaning to. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topics` | string | no | Optional topic words used to rank meaning results, with at most five words. |
| `spellingPattern` | string | no | Optional spelling pattern to combine with the meaning constraint. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `score` | number | Datamuse ranking score when provided. |
| `tags` | array<string> | Optional metadata tags returned by Datamuse. |
| `word` | string | Matching word or phrase. |

## Native endpoint

Through the native Datamuse API, this operation is `GET /words` (base URL `https://api.datamuse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-words-by-meaning.md) for the provider-specific parameters and requirements.

