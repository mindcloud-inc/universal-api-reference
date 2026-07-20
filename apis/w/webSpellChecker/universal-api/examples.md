# WebSpellChecker Universal API Examples

These examples use the MindCloud API key and WebSpellChecker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Info

Retrieves subscription details from WebSpellChecker.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/get-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/get-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "banner": true,
      "canRemoveBranding": true,
      "cdModificationTime": 1,
      "freeze": 1,
      "generateLangList": {},
      "grammarLangList": {},
      "langList": {},
      "maxGenerateInputSize": 1,
      "minGenerateInputSize": 1,
      "programVersion": "string",
      "prompts": {},
      "sendStatistics": true,
      "session": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Info action reference](actions/get-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webSpellChecker/latest/actions/get-info).

## Add User Dictionary Word

Adds a word to a user dictionary in WebSpellChecker.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/add-user-dictionary-word" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "dictionary_to_update",
  "word": "word_to_add"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/add-user-dictionary-word', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "dictionary_to_update",
    "word": "word_to_add"
  })
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Add User Dictionary Word action reference](actions/add-user-dictionary-word.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webSpellChecker/latest/actions/add-user-dictionary-word).
