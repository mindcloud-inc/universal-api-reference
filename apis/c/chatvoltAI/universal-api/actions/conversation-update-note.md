# Chatvolt AI: Update Note

Updates a note in Chatvolt AI.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-update-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "noteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-update-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "noteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | ID of the conversation. |
| `noteId` | string | yes | ID of the note to update. |
| `note` | string | no | Updated text content of the note. |
| `isPrivate` | boolean | no | Updated privacy status. |
| `notificationDateTime` | string | no | Updated notification date and time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversationId": "string",
      "createdAt": "string",
      "id": "string",
      "isJustification": true,
      "isPrivate": true,
      "note": "string",
      "notificationDateTime": "string",
      "organizationId": "string",
      "sendDesktopNotification": true,
      "updatedAt": "string",
      "userEmail": "ava@example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversationId` | string | ConversationId. |
| `createdAt` | string | CreatedAt. |
| `id` | string | Id. |
| `isJustification` | boolean | IsJustification. |
| `isPrivate` | boolean | IsPrivate. |
| `note` | string | Note. |
| `notificationDateTime` | string | NotificationDateTime. |
| `organizationId` | string | OrganizationId. |
| `sendDesktopNotification` | boolean | SendDesktopNotification. |
| `updatedAt` | string | UpdatedAt. |
| `userEmail` | string | UserEmail. |
| `userId` | string | UserId. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `PUT /conversations/{conversationId}/notes/{noteId}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/conversation-update-note.md) for the provider-specific parameters and requirements.

