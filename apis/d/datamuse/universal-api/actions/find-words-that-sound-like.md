# Datamuse: Find Words That Sound Like

Finds words in Datamuse by pronunciation similarity.

```
GET https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-words-that-sound-like
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datamuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-words-that-sound-like?connectionId=$CONNECTION_ID&soundsLike=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "soundsLike": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-words-that-sound-like?${params}`, {
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
| `soundsLike` | string | yes | Text that the results should be pronounced similarly to. |

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
| `numSyllables` | number | Optional syllable count returned for sound-like results. |
| `score` | number | Datamuse ranking score when provided. |
| `word` | string | Matching word or phrase. |

## Native endpoint

Through the native Datamuse API, this operation is `GET /words` (base URL `https://api.datamuse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-words-that-sound-like.md) for the provider-specific parameters and requirements.

