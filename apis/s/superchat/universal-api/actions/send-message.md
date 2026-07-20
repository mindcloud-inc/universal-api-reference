# Superchat: Send Message

Sends a message to a contact in Superchat.

```
POST https://connect.mindcloud.co/v1/universal/superchat/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superchat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superchat/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to[]": [
    {}
  ],
  "from.channel_id": "string",
  "content": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superchat/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to[]": [{}],
    "from.channel_id": "string",
    "content": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to[]` | array<object> | yes |  |
| `from.channel_id` | string | yes | Unique identifier of the channel. Always bears prefix 'mc_' |
| `content` | object | yes | Use the media object to send images, videos, audio files or documents. You have to upload the file via POST `/files` first. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from.name` | string | no |  |
| `in_reply_to` | string | no | Message ID of the message the newly sent message will be a reply to. Only supported for email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "conversation_id": "string",
      "created_at": "string",
      "direction": "string",
      "from": {
        "channel_id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "in_reply_to": "string",
      "status": "string",
      "to": {
        "contact_id": "string",
        "identifier": "string",
        "url": "https://example.com"
      },
      "updated_at": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object |  |
| `conversation_id` | string |  |
| `created_at` | string |  |
| `direction` | string |  |
| `from` | object |  |
| `from.channel_id` | string |  |
| `from.name` | string |  |
| `id` | string |  |
| `in_reply_to` | string |  |
| `status` | string |  |
| `to` | array<object> |  |
| `to.contact_id` | string |  |
| `to.identifier` | string |  |
| `to.url` | string |  |
| `updated_at` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Superchat API, this operation is `POST /messages` (base URL `https://api.superchat.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

