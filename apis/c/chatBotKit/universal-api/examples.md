# ChatBotKit Universal API Examples

These examples use the MindCloud API key and ChatBotKit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bots



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-bots?${params}`, {
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
      "cursor": "string",
      "items": [
        {
          "backstory": "string",
          "blueprintId": "string",
          "createdAt": 1,
          "datasetId": "string",
          "description": "string",
          "id": "string",
          "model": "string",
          "moderation": true,
          "name": "Ava Chen",
          "privacy": true,
          "skillsetId": "string",
          "updatedAt": 1,
          "visibility": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Bots action reference](actions/list-bots.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatBotKit/latest/actions/list-bots).

## Complete Conversation Interaction



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/complete-conversation-interaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/complete-conversation-interaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": ["string"]
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
      "end": {
        "reason": "string"
      },
      "text": "string",
      "usage": {
        "token": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Complete Conversation Interaction action reference](actions/complete-conversation-interaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatBotKit/latest/actions/complete-conversation-interaction).
