# Datamuse: Find Consonant Matches

Finds consonant matches in Datamuse for a given word.

```
GET https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-consonant-matches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datamuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-consonant-matches?connectionId=$CONNECTION_ID&word=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "word": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-consonant-matches?${params}`, {
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
| `word` | string | yes | Word to find consonant matches for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "numSyllables": 1,
      "score": 1,
      "word": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numSyllables` | number | Optional syllable count returned for consonant matches. |
| `score` | number | Datamuse ranking score when provided. |
| `word` | string | Matching word or phrase. |

## Native endpoint

Through the native Datamuse API, this operation is `GET /words` (base URL `https://api.datamuse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-consonant-matches.md) for the provider-specific parameters and requirements.

