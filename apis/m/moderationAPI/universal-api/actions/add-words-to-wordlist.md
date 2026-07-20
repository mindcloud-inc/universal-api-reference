# Moderation API: Add Words To Wordlist

Adds words to a wordlist in Moderation API.

```
POST https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/add-words-to-wordlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/add-words-to-wordlist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "words[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/add-words-to-wordlist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "words[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the wordlist to add words to |
| `words[]` | array<string> | yes | Array of words to add to the wordlist. Duplicate words will be ignored. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedCount": 1,
      "addedWords": [
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
| `addedCount` | number | Number of words added |
| `addedWords` | array<string> | List of words that were added |
| `totalCount` | number | Total number of words in wordlist |

## Native endpoint

Through the native Moderation API API, this operation is `POST /wordlist/:id/words` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-words-to-wordlist.md) for the provider-specific parameters and requirements.

