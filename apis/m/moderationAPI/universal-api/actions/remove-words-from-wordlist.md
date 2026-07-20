# Moderation API: Remove Words From Wordlist

Removes words from a wordlist in Moderation API.

```
DELETE https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/remove-words-from-wordlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/remove-words-from-wordlist?connectionId=$CONNECTION_ID&id=string&words%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "words[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/remove-words-from-wordlist?${params}`, {
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
| `id` | string | yes | ID of the wordlist to remove words from |
| `words[]` | array<string> | yes | Array of words to remove from the wordlist |

## Response

```json
{
  "success": true,
  "data": [
    {
      "removedCount": 1,
      "removedWords": [
        "string"
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
| `removedCount` | number | Number of words removed |
| `removedWords` | array<string> | List of words removed |
| `totalCount` | number | Total number of words in wordlist |

## Native endpoint

Through the native Moderation API API, this operation is `DELETE /wordlist/:id/words` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-words-from-wordlist.md) for the provider-specific parameters and requirements.

