# Dust Universal API Examples

These examples use the MindCloud API key and Dust connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agents

Retrieves agent configurations from the Dust workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dust/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dust/latest/actions/list-agents?${params}`, {
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
      "agentConfigurations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Agents action reference](actions/list-agents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dust/latest/actions/list-agents).

## Create Conversation

Creates a new conversation in Dust.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dust/latest/actions/create-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dust/latest/actions/create-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
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
      "conversation": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Conversation action reference](actions/create-conversation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dust/latest/actions/create-conversation).
