# WebSpellChecker: Rename User Dictionary

Renames a user dictionary in WebSpellChecker.

```
PUT https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/rename-user-dictionary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebSpellChecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/rename-user-dictionary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "existing_dictionary",
  "newName": "renamed_dictionary"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/rename-user-dictionary', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "existing_dictionary",
    "newName": "renamed_dictionary"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Existing dictionary name. Example: `existing_dictionary`. |
| `newName` | string | yes | New name for the dictionary. Example: `renamed_dictionary`. |

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
| `name` | string | Dictionary name after the rename. |
| `wordlist` | array<string> | Words affected by the action. |

## Native endpoint

Through the native WebSpellChecker API, this operation is `GET /` (base URL `https://svc.webspellchecker.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-user-dictionary.md) for the provider-specific parameters and requirements.

