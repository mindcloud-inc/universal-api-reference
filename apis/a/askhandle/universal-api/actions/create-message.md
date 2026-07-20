# AskHandle: Create Message

Creates a new message in an AskHandle room.

```
POST https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AskHandle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/create-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | Message body. |
| `email` | string | no | Message sender email. |
| `nickname` | string | no | Message sender nickname. |
| `room.uuid` | string | no | The UUID of the room that will receive the message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "email": "ava@example.com",
      "isSupportSender": true,
      "nickname": "Ava Chen",
      "phoneNumber": "string",
      "sentAt": "2026-05-07T12:00:00.000Z",
      "supportAnswer": "string",
      "terminated": true,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string | Message body. |
| `email` | string | Message sender email. |
| `isSupportSender` | boolean | Whether the sender is support. |
| `nickname` | string | Message sender nickname. |
| `phoneNumber` | string | Sender phone number. |
| `sentAt` | date | Sent timestamp. |
| `supportAnswer` | string | AskHandle support answer. |
| `terminated` | boolean | Whether the session is terminated. |
| `uuid` | string | Message UUID. |

## Native endpoint

Through the native AskHandle API, this operation is `POST /messages/` (base URL `https://dashboard.askhandle.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.

