# Colossyan Universal API Examples

These examples use the MindCloud API key and Colossyan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Voices

Retrieves available voices from Colossyan.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/list-voices?${params}`, {
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
      "ages": [
        "string"
      ],
      "characters": [
        "string"
      ],
      "displayName": "Ava Chen",
      "features": {},
      "genders": [
        "string"
      ],
      "isClonedVoice": true,
      "languages": [
        "string"
      ],
      "name": "Ava Chen",
      "sample": "string",
      "scenarios": [
        "string"
      ],
      "style": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Voices action reference](actions/list-voices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/colossyan/latest/actions/list-voices).

## Create Avatar

Creates a new avatar in Colossyan.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/create-avatar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "displayName": "Ava Chen",
  "sourceFileUrl": "https://example.com",
  "gender": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/create-avatar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "displayName": "Ava Chen",
    "sourceFileUrl": "https://example.com",
    "gender": "0"
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
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Avatar action reference](actions/create-avatar.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/colossyan/latest/actions/create-avatar).
