# GPT Chatbot Universal API Examples

These examples use the MindCloud API key and GPT Chatbot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Chatbots

Retrieves the current user's chatbots from GPT Chatbot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-chatbots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-chatbots?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "meta": {},
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Chatbots action reference](actions/list-chatbots.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gPTChatbot/latest/actions/list-chatbots).

## Create Agent

Creates an agent for a chatbot in GPT Chatbot.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatbotUuid": "string",
  "name": "Ava Chen",
  "type": "string",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatbotUuid": "string",
    "name": "Ava Chen",
    "type": "string",
    "description": "string"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataSourceUuids": [
        "string"
      ],
      "description": "string",
      "enabled": true,
      "meta": {},
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "prompt": "string",
      "toolFunctions": [
        {}
      ],
      "type": "string",
      "uuid": "string",
      "variables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Agent action reference](actions/create-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gPTChatbot/latest/actions/create-agent).
