# Datamuse: Find Contextual Words

Finds contextual words in Datamuse by sentence context.

```
GET https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-contextual-words
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datamuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-contextual-words?connectionId=$CONNECTION_ID&leftContext=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leftContext": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-contextual-words?${params}`, {
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
| `leftContext` | string | yes | Word immediately to the left of the target word in a sentence. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rightContext` | string | no | Word immediately to the right of the target word in a sentence. |
| `spellingPattern` | string | no | Optional spelling constraint or wildcard pattern for contextual results. |
| `topics` | string | no | Optional topic words to skew results toward, with at most five words. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `score` | number | Datamuse ranking score when provided. |
| `word` | string | Matching word or phrase. |

## Native endpoint

Through the native Datamuse API, this operation is `GET /words` (base URL `https://api.datamuse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-contextual-words.md) for the provider-specific parameters and requirements.

