# Chaindesk Universal API Examples

These examples use the MindCloud API key and Chaindesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Conversations

Retrieves conversations from your Chaindesk workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-conversations?${params}`, {
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
      "agent": {
        "createdAt": "string",
        "description": "string",
        "formId": "string",
        "handle": "string",
        "hidden": true,
        "iconUrl": "https://example.com",
        "id": "string",
        "includeSources": true,
        "interfaceConfig": {},
        "modelName": "Ava Chen",
        "name": "Ava Chen",
        "nbQueries": 1,
        "organizationId": "string",
        "ownerId": "string",
        "prompt": "string",
        "promptType": "string",
        "restrictKnowledge": true,
        "systemPrompt": "string",
        "temperature": 1,
        "updatedAt": "string",
        "useLanguageDetection": true,
        "useMarkdown": true,
        "userPrompt": "string",
        "visibility": "string"
      },
      "agentId": "string",
      "channel": "string",
      "channelCredentialsId": "string",
      "channelExternalId": "string",
      "createdAt": "string",
      "formId": "string",
      "id": "string",
      "isAiEnabled": true,
      "mailInboxId": "string",
      "messages": {
        "agentId": "string",
        "contactId": "string",
        "conversationId": "string",
        "createdAt": "string",
        "eval": "string",
        "externalId": "string",
        "from": "string",
        "html": "string",
        "id": "string",
        "inputId": "string",
        "metadata": "string",
        "read": true,
        "sources": "string",
        "text": "string",
        "updatedAt": "string",
        "usage": "string",
        "userId": "string",
        "visitorId": "string"
      },
      "metadata": {
        "country": "string"
      },
      "organizationId": "string",
      "priority": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "string",
      "userId": "string",
      "visitorId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Conversations action reference](actions/list-conversations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chaindesk/latest/actions/list-conversations).

## Continue Agent Conversation

Sends a follow-up query in a Chaindesk conversation.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/continue-agent-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "conversationId": "string",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/continue-agent-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "conversationId": "string",
    "query": "string"
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
      "answer": "string",
      "approvals": [
        "string"
      ],
      "conversationId": "string",
      "messageId": "string",
      "sources": [
        "string"
      ],
      "usage": {
        "completionTokens": 1,
        "cost": 1,
        "promptTokens": 1,
        "totalTokens": 1
      },
      "visitorId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Continue Agent Conversation action reference](actions/continue-agent-conversation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chaindesk/latest/actions/continue-agent-conversation).
