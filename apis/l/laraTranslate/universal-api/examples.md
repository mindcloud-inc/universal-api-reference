# Lara Translate Universal API Examples

These examples use the MindCloud API key and Lara Translate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List supported languages

Retrieves supported languages from Lara Translate.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/list-supported-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/list-supported-languages?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [List supported languages action reference](actions/list-supported-languages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/laraTranslate/latest/actions/list-supported-languages).

## Add translation unit to memory

Adds a translation unit to a Lara Translate memory.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/add-translation-unit-to-memory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "mem_123",
  "source": "en-US",
  "target": "it-IT",
  "sentence": "string",
  "translation": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/add-translation-unit-to-memory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "mem_123",
    "source": "en-US",
    "target": "it-IT",
    "sentence": "string",
    "translation": "string"
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
      "begin": 1,
      "channel": 1,
      "end": 1,
      "id": "string",
      "progress": 1,
      "size": 1
    }
  ],
  "meta": {}
}
```

See the full [Add translation unit to memory action reference](actions/add-translation-unit-to-memory.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/laraTranslate/latest/actions/add-translation-unit-to-memory).
