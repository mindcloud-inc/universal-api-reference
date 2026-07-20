# Datamuse: Get Spanish Word Suggestions

Retrieves Spanish word suggestions from Datamuse for partial search text.

```
GET https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/get-spanish-word-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datamuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/get-spanish-word-suggestions?connectionId=$CONNECTION_ID&searchText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/get-spanish-word-suggestions?${params}`, {
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
| `searchText` | string | yes | Partial Spanish text entered by the user for autocomplete suggestions. |

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
| `score` | number | Datamuse suggestion ranking score. |
| `word` | string | Suggested Spanish completion. |

## Native endpoint

Through the native Datamuse API, this operation is `GET /sug` (base URL `https://api.datamuse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-spanish-word-suggestions.md) for the provider-specific parameters and requirements.

