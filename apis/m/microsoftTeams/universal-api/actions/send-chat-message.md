# Microsoft Teams: Send Chat Message

Creates a new chat message in Microsoft Teams.

```
POST https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/send-chat-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/send-chat-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string",
  "body.content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/send-chat-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string",
    "body.content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | Microsoft Graph chat ID. |
| `body.content` | string | yes | Chat message body content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "body": {},
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "deletedDateTime": "2026-05-07T12:00:00.000Z",
      "etag": "string",
      "from": {},
      "id": "string",
      "importance": "string",
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "locale": "string",
      "mentions": [
        {}
      ],
      "messageType": "string",
      "reactions": [
        {}
      ],
      "replyToId": "string",
      "subject": "string",
      "summary": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> | Message attachments. |
| `body` | object | Message body content. |
| `createdDateTime` | date | Timestamp at which the message was created. |
| `deletedDateTime` | date | Timestamp at which the message was deleted, when applicable. |
| `etag` | string | Version tag for the message. |
| `from` | object | Sender identity. |
| `id` | string | Unique identifier for the message. |
| `importance` | string | Importance of the message. |
| `lastModifiedDateTime` | date | Timestamp at which the message was last modified. |
| `locale` | string | Locale of the message. |
| `mentions` | array<object> | Mentions included in the message. |
| `messageType` | string | Type of chat message. |
| `reactions` | array<object> | Message reactions. |
| `replyToId` | string | ID of the parent message when this item is a reply. |
| `subject` | string | Subject of the message. |
| `summary` | string | Summary text for the message. |
| `webUrl` | string | Link to the message in Microsoft Teams. |

## Native endpoint

Through the native Microsoft Teams API, this operation is `POST /v1.0/chats/:chatId/messages` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-chat-message.md) for the provider-specific parameters and requirements.

