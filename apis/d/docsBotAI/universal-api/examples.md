# DocsBot AI Universal API Examples

These examples use the MindCloud API key and DocsBot AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams

Retrieves teams from DocsBot AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/list-teams?${params}`, {
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
      "botCount": 1,
      "chunkCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "openAIKey": "string",
      "pageCount": 1,
      "plan": {},
      "questionCount": 1,
      "roles": {},
      "sourceCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docsBotAI/latest/actions/list-teams).

## Create Bot

Creates a new bot in DocsBot AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/create-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/create-bot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string"
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
      "chunkCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customPrompt": "string",
      "description": "string",
      "id": "string",
      "indexId": "string",
      "language": "string",
      "model": "string",
      "name": "Ava Chen",
      "pageCount": 1,
      "privacy": "string",
      "questionCount": 1,
      "sourceCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Bot action reference](actions/create-bot.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docsBotAI/latest/actions/create-bot).
