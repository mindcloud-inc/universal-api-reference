# Chatvolt AI: Create Note

Creates a note in Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/conversation-create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "note": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | ID of the conversation to add a note to. |
| `note` | string | yes | Text content of the note (max 500 characters). |
| `isPrivate` | boolean | no | Whether the note is private. |
| `isJustify` | boolean | no | Whether the note is a justification (admin only). |
| `notificationDateTime` | string | no | Date and time for a notification, if any. |

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

Through the native Chatvolt AI API, this operation is `POST /conversations/{conversationId}/notes` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/conversation-create-note.md) for the provider-specific parameters and requirements.

