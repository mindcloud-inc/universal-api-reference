# SuperOps IT: Create Ticket Conversation



```
POST https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-ticket-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-ticket-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/create-ticket-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | The SuperOps ticket ID. |
| `content` | string | yes | The conversation content. |
| `userId` | string | no | Optional user ID creating the conversation. |
| `time` | date | no | Optional conversation creation time in ISO 8601 format. |
| `sendMail` | boolean | no | Whether SuperOps should send mail for the conversation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTicketConversation": {
        "content": "string",
        "conversationId": "string",
        "time": "2026-05-07T12:00:00.000Z",
        "type": "string",
        "user": {
          "email": "ava@example.com",
          "name": "Ava Chen",
          "userId": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTicketConversation.content` | string |  |
| `createTicketConversation.conversationId` | string |  |
| `createTicketConversation.time` | date |  |
| `createTicketConversation.type` | string |  |
| `createTicketConversation.user.email` | string |  |
| `createTicketConversation.user.name` | string |  |
| `createTicketConversation.user.userId` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket-conversation.md) for the provider-specific parameters and requirements.

