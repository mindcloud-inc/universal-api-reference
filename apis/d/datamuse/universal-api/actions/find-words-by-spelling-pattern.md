# Datamuse: Find Words By Spelling Pattern

Finds words in Datamuse by spelling pattern.

```
GET https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-words-by-spelling-pattern
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datamuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-words-by-spelling-pattern?connectionId=$CONNECTION_ID&spellingPattern=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spellingPattern": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-words-by-spelling-pattern?${params}`, {
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
| `spellingPattern` | string | yes | Spelling constraint or wildcard pattern. Use * for any number of characters and ? for one character. |

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

Through the native Datamuse API, this operation is `GET /words` (base URL `https://api.datamuse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-words-by-spelling-pattern.md) for the provider-specific parameters and requirements.

