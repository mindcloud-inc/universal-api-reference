# LMNT Universal API Examples

These examples use the MindCloud API key and LMNT connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Account Info

Retrieves your account details from LMNT.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/account-info?${params}`, {
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
      "plan": {
        "character_limit": 1,
        "commercial_use_allowed": true,
        "professional_voice_limit": 1,
        "type": "string"
      },
      "usage": {
        "characters": 1,
        "credit_characters": 1,
        "instant_voices": 1,
        "period_end": 1,
        "professional_voices": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Account Info action reference](actions/account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lMNT/latest/actions/account-info).

## Create Voice

Creates a new voice in LMNT.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/create-voice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "enhance": true,
  "files": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/create-voice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "enhance": true,
    "files": "string",
    "name": "Ava Chen"
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
      "gender": "string",
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "preview_url": "https://example.com",
      "starred": true,
      "state": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Voice action reference](actions/create-voice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lMNT/latest/actions/create-voice).
