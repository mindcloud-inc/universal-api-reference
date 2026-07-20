# Tidio: Ask Lyro [Plus plan]

Asks Lyro to answer a ticket in Tidio.

```
POST https://connect.mindcloud.co/v1/universal/tidio/latest/actions/ask-lyro-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/ask-lyro-plus-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticketId": "string",
  "subject": "string",
  "contactEmail": "ava@example.com",
  "contactName": "Ava Chen",
  "recipientEmail": "ava@example.com",
  "messages": {},
  "messages[].createdAt": "2026-05-07T12:00:00.000Z",
  "messages[].messageId": "string",
  "messages[].authorType": "string",
  "messages[].messageType": "string",
  "messages[].messageContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidio/latest/actions/ask-lyro-plus-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticketId": "string",
    "subject": "string",
    "contactEmail": "ava@example.com",
    "contactName": "Ava Chen",
    "recipientEmail": "ava@example.com",
    "messages": {},
    "messages[].createdAt": "2026-05-07T12:00:00.000Z",
    "messages[].messageId": "string",
    "messages[].authorType": "string",
    "messages[].messageType": "string",
    "messages[].messageContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticketId` | string | yes | Tidio ticket identifier to answer with Lyro. |
| `subject` | string | yes | Ticket subject shown to Lyro. |
| `contactEmail` | string | yes | Email address of the contact tied to the ticket. |
| `contactName` | string | yes | Display name of the contact tied to the ticket. |
| `recipientEmail` | string | yes | Recipient email where the Lyro answer will be sent. |
| `messages` | list<object> | yes | Conversation messages used as Lyro context. |
| `messages[].createdAt` | date | yes | Message creation timestamp in ISO 8601 format. |
| `messages[].messageId` | string | yes | Unique ULID of the conversation message. |
| `messages[].authorType` | string | yes | Message author type. Tidio currently accepts contact only. |
| `messages[].messageType` | string | yes | Message visibility type. Tidio currently accepts public only. |
| `messages[].attachments` | list<string> | no | Optional attachment URLs for the message. |
| `messages[].messageContent` | string | yes | Body text of the conversation message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageContent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageContent` | string | Message content |

## Native endpoint

Through the native Tidio API, this operation is `POST /lyro/tickets` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ask-lyro-plus-plan.md) for the provider-specific parameters and requirements.

