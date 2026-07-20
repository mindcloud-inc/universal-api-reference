# Simpleen Translation Universal API Examples

These examples use the MindCloud API key and Simpleen Translation connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Languages

Retrieves languages from Simpleen Translation.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/list-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/list-languages?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Languages action reference](actions/list-languages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simpleenTranslation/latest/actions/list-languages).

## Create File

Creates a new file in Simpleen Translation.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/create-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "dataformat": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/create-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "dataformat": "string"
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
      "cntSegments": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "dataformat": "string",
      "filepath": "string",
      "formality": "string",
      "id": 1,
      "interpolation": "string",
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create File action reference](actions/create-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simpleenTranslation/latest/actions/create-file).
