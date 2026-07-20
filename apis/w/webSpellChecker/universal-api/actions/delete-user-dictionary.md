# WebSpellChecker: Delete User Dictionary

Deletes an existing user dictionary from WebSpellChecker.

```
DELETE https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/delete-user-dictionary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebSpellChecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/delete-user-dictionary?connectionId=$CONNECTION_ID&name=dictionary_to_delete" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "dictionary_to_delete"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/delete-user-dictionary?${params}`, {
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
| `name` | string | yes | Name of the dictionary to delete. Example: `dictionary_to_delete`. |

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
| `action` | string | Executed user_dictionary action. |
| `modificationTime` | number | Dictionary modification timestamp or zero after deletion. |
| `name` | string | Dictionary name. |
| `wordlist` | array<string> | Words affected by the action. |

## Native endpoint

Through the native WebSpellChecker API, this operation is `GET /` (base URL `https://svc.webspellchecker.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user-dictionary.md) for the provider-specific parameters and requirements.

