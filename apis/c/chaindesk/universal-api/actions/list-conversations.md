# Chaindesk: List Conversations

Retrieves conversations from your Chaindesk workspace.

```
GET https://connect.mindcloud.co/v1/universal/chaindesk/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chaindesk `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `take` | number | no |  |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object |  |
| `agent.createdAt` | string |  |
| `agent.description` | string |  |
| `agent.formId` | string |  |
| `agent.handle` | string |  |
| `agent.hidden` | boolean |  |
| `agent.iconUrl` | string |  |
| `agent.id` | string |  |
| `agent.includeSources` | boolean |  |
| `agent.interfaceConfig` | object |  |
| `agent.modelName` | string |  |
| `agent.name` | string |  |
| `agent.nbQueries` | number |  |
| `agent.organizationId` | string |  |
| `agent.ownerId` | string |  |
| `agent.prompt` | string |  |
| `agent.promptType` | string |  |
| `agent.restrictKnowledge` | boolean |  |
| `agent.systemPrompt` | string |  |
| `agent.temperature` | number |  |
| `agent.updatedAt` | string |  |
| `agent.useLanguageDetection` | boolean |  |
| `agent.useMarkdown` | boolean |  |
| `agent.userPrompt` | string |  |
| `agent.visibility` | string |  |
| `agentId` | string |  |
| `channel` | string |  |
| `channelCredentialsId` | string |  |
| `channelExternalId` | string |  |
| `createdAt` | string |  |
| `formId` | string |  |
| `id` | string |  |
| `isAiEnabled` | boolean |  |
| `mailInboxId` | string |  |
| `messages` | array<object> |  |
| `messages.agentId` | string |  |
| `messages.contactId` | string |  |
| `messages.conversationId` | string |  |
| `messages.createdAt` | string |  |
| `messages.eval` | string |  |
| `messages.externalId` | string |  |
| `messages.from` | string |  |
| `messages.html` | string |  |
| `messages.id` | string |  |
| `messages.inputId` | string |  |
| `messages.metadata` | string |  |
| `messages.read` | boolean |  |
| `messages.sources` | string |  |
| `messages.text` | string |  |
| `messages.updatedAt` | string |  |
| `messages.usage` | string |  |
| `messages.userId` | string |  |
| `messages.visitorId` | string |  |
| `metadata` | object |  |
| `metadata.country` | string |  |
| `organizationId` | string |  |
| `priority` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `userId` | string |  |
| `visitorId` | string |  |

## Native endpoint

Through the native Chaindesk API, this operation is `GET /conversations` (base URL `https://app.chaindesk.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

