# Datamuse: Find Nouns For Adjective

Finds nouns often described by an adjective in Datamuse.

```
GET https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-nouns-for-adjective
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datamuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-nouns-for-adjective?connectionId=$CONNECTION_ID&adjective=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adjective": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datamuse/latest/actions/find-nouns-for-adjective?${params}`, {
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
| `adjective` | string | yes | Adjective to find nouns it commonly modifies. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topics` | string | no | Optional topic words used to rank noun results. |

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

Through the native Datamuse API, this operation is `GET /words` (base URL `https://api.datamuse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-nouns-for-adjective.md) for the provider-specific parameters and requirements.

