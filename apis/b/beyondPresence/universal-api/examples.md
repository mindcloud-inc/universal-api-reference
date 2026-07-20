# Beyond Presence Universal API Examples

These examples use the MindCloud API key and Beyond Presence connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify API Key

Verifies a Beyond Presence API key.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/verify-api-key?${params}`, {
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

See the full [Verify API Key action reference](actions/verify-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/beyondPresence/latest/actions/verify-api-key).

## Create Agent

Creates a new agent in Beyond Presence.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "avatarId": "string",
  "name": "Ava Chen",
  "systemPrompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "avatarId": "string",
    "name": "Ava Chen",
    "systemPrompt": "string"
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
      "avatarId": "string",
      "capabilities": [
        {}
      ],
      "greeting": "string",
      "id": "string",
      "knowledgeFileIds": [
        "string"
      ],
      "language": "string",
      "llm": {},
      "maxSessionLengthMinutes": 1,
      "name": "Ava Chen",
      "systemPrompt": "string",
      "tts": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Agent action reference](actions/create-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/beyondPresence/latest/actions/create-agent).
