# Callbell: Send Message

Creates a new outbound message in Callbell.

```
POST https://connect.mindcloud.co/v1/universal/callbell/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callbell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callbell/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelUuid": "string",
  "from": "string",
  "to": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callbell/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelUuid": "string",
    "from": "string",
    "to": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedUser` | string | no | Collaborator email to assign to the message. |
| `botStatus` | string | no | Bot status to apply to the contact after sending. |
| `channelUuid` | string | yes | Channel UUID to send the message from. |
| `content.text` | string | no | Text body for text messages. |
| `content.url` | string | no | Public URL for media messages. |
| `fields` | string | no | Comma-separated related resources to include in the response. |
| `from` | string | yes | Channel type such as whatsapp. |
| `metadata` | object | no | Metadata object to attach to the message. |
| `optinContact` | boolean | no | Confirm that the contact opted in to receive messages. |
| `teamUuid` | string | no | Team UUID to assign to the message. |
| `templateUuid` | string | no | Template UUID for WhatsApp template messages. |
| `templateValues[]` | array<string> | no | Template variable values in order. |
| `to` | string | yes | Destination phone number or platform identifier. |
| `type` | string | yes | Type of message to send. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {},
      "conversation": {},
      "messageStatusPayload": {},
      "status": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object |  |
| `conversation` | object |  |
| `messageStatusPayload` | object |  |
| `status` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Callbell API, this operation is `POST /messages/send` (base URL `https://api.callbell.eu/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

