# WebSpellChecker: Delete User Dictionary Word

Deletes a word from a user dictionary in WebSpellChecker.

```
PUT https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/delete-user-dictionary-word
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebSpellChecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/delete-user-dictionary-word" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "dictionary_to_update",
  "word": "word_to_remove"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/delete-user-dictionary-word', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "dictionary_to_update",
    "word": "word_to_remove"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the dictionary to update. Example: `dictionary_to_update`. |
| `word` | string | yes | Single word to remove from the dictionary. Example: `word_to_remove`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "modificationTime": 1,
      "name": "Ava Chen",
      "wordlist": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string | Performed dictionary action. |
| `modificationTime` | number | Dictionary modification timestamp. |
| `name` | string | Dictionary name. |
| `wordlist` | array<string> | Affected word list. |

## Native endpoint

Through the native WebSpellChecker API, this operation is `GET /` (base URL `https://svc.webspellchecker.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user-dictionary-word.md) for the provider-specific parameters and requirements.

