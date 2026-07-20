# Chatvolt AI: Get Conversation By Id

Retrieves a conversation from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-get-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-get-by-id?connectionId=$CONNECTION_ID&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-get-by-id?${params}`, {
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
| `conversationId` | string | yes | ID of the conversation to be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "assignees": [
        {}
      ],
      "channel": "string",
      "channelCredentialsId": "string",
      "channelExternalId": "string",
      "conversationContexts": [
        {}
      ],
      "conversationVariables": [
        "string"
      ],
      "createdAt": "string",
      "crmScenarioConversations": [
        {}
      ],
      "formId": "string",
      "frustration": 1,
      "id": "string",
      "isAiEnabled": true,
      "mailInboxId": "string",
      "metadata": {},
      "organizationId": "string",
      "participantsContacts": [
        "string"
      ],
      "priority": "string",
      "status": "string",
      "tags": [
        {}
      ],
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
| `agentId` | string | The ID of the agent handling the conversation |
| `assignees` | array<object> | List of assignees for the conversation. |
| `channel` | string | The channel through which the conversation took place (e.g., 'dashboard', 'whatsapp') |
| `channelCredentialsId` | string | ID of the credentials used for the channel |
| `channelExternalId` | string | External ID of the channel, if any |
| `conversationContexts` | array<object> | List of contexts associated with the conversation. |
| `conversationVariables` | array | List of variables associated with the conversation |
| `createdAt` | string | The date and time when the conversation was created |
| `crmScenarioConversations` | array<object> | Lista de vínculos entre a conversa e cenários CRM. |
| `formId` | string | ID of the form used, if any |
| `frustration` | number | Frustration level of the conversation, if applicable |
| `id` | string | The unique identifier for the conversation |
| `isAiEnabled` | boolean | Indicates whether AI is enabled for the conversation |
| `mailInboxId` | string | The mailbox ID, if relevant |
| `metadata` | object | Metadata associated with the conversation, if any |
| `organizationId` | string | The organization ID associated with the conversation |
| `participantsContacts` | array | List of contacts associated with the conversation |
| `priority` | string | The priority of the conversation |
| `status` | string | The current status of the conversation |
| `tags` | array<object> | List of tags associated with the conversation. |
| `title` | string | The title of the conversation, if available |
| `updatedAt` | string | The date and time when the conversation was last updated |
| `userId` | string | The ID of the user associated with the conversation |
| `visitorId` | string | The ID of the visitor, if applicable |

## Native endpoint

Through the native Chatvolt AI API, this operation is `GET /conversation/{conversationId}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/conversation-get-by-id.md) for the provider-specific parameters and requirements.

