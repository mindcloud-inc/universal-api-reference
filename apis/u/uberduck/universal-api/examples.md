# Uberduck Universal API Examples

These examples use the MindCloud API key and Uberduck connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Models

Retrieves available TTS models from Uberduck.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/get-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/get-models?${params}`, {
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
      "models": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Models action reference](actions/get-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uberduck/latest/actions/get-models).

## Instant Voice Clone

Creates a zero-shot voice in Uberduck.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/instant-voice-clone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "paths": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uberduck/latest/actions/instant-voice-clone', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "paths": "string"
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
      "description": "string",
      "displayName": "Ava Chen",
      "isPrivate": true,
      "name": "Ava Chen",
      "sampleUrl": "https://example.com",
      "tags": [
        "string"
      ],
      "voicemodelUuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Instant Voice Clone action reference](actions/instant-voice-clone.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uberduck/latest/actions/instant-voice-clone).
