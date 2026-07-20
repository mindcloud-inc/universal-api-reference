# WebSpellChecker: Get User Dictionary

Retrieves a user dictionary wordlist from WebSpellChecker.

```
GET https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/get-user-dictionary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebSpellChecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/get-user-dictionary?connectionId=$CONNECTION_ID&name=dictionary_to_load" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "dictionary_to_load"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/get-user-dictionary?${params}`, {
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
| `name` | string | yes | Name of the dictionary to load. Example: `dictionary_to_load`. |

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
| `modificationTime` | number | Dictionary modification timestamp. |
| `name` | string | Dictionary name. |
| `wordlist` | array<string> | Words present in the dictionary. |

## Native endpoint

Through the native WebSpellChecker API, this operation is `GET /` (base URL `https://svc.webspellchecker.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-dictionary.md) for the provider-specific parameters and requirements.

