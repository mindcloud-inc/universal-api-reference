# WotNot: Start WhatsApp Conversation

Creates a WhatsApp conversation in WotNot.

```
POST https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/start-whats-app-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/start-whats-app-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to.phone": "string",
  "message.data.template": "string",
  "assignee": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/start-whats-app-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "to.phone": "string",
    "message.data.template": "string",
    "assignee": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | Configured WhatsApp sender number |
| `to.phone` | string | yes | Recipient phone number |
| `to.name` | string | no | Recipient display name |
| `to.email` | string | no | Recipient email |
| `message.data.template` | string | yes | Approved WhatsApp template name |
| `assignee` | string | yes | Assigned agent email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "phone": "string"
      },
      "conversation": {
        "assignee": {
          "id": 1,
          "to": "string"
        },
        "created_at": "string",
        "id": "string",
        "message_id": "string"
      },
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.email` | string |  |
| `contact.id` | string |  |
| `contact.name` | string |  |
| `contact.phone` | string |  |
| `conversation.assignee.id` | number |  |
| `conversation.assignee.to` | string |  |
| `conversation.created_at` | string |  |
| `conversation.id` | string |  |
| `conversation.message_id` | string |  |
| `ok` | boolean |  |

## Native endpoint

Through the native WotNot API, this operation is `POST /api/v1/conversations` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-whats-app-conversation.md) for the provider-specific parameters and requirements.

