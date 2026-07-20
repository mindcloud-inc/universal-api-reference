# Heyy: Send WhatsApp Message

Sends a WhatsApp message from a Heyy channel.

```
POST https://connect.mindcloud.co/v1/universal/heyy/latest/actions/send-whats-app-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/send-whats-app-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "messageTemplateId": "string",
  "phoneNumber": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyy/latest/actions/send-whats-app-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "messageTemplateId": "string",
    "phoneNumber": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | The channel ID. |
| `fileId` | string | no | Optional uploaded file ID. |
| `phoneNumber` | string | yes | The destination phone number. |
| `scheduledAt` | string | no | Optional scheduled send time in ISO 8601 format. |
| `type` | string | yes | The WhatsApp message type. |
| `variables[]` | array<object> | no | Optional template variables. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageTemplateId` | string | yes | The Heyy message template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "chatId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string |  |
| `chatId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Heyy API, this operation is `POST /[:channelId]/whatsapp_messages/send` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-whats-app-message.md) for the provider-specific parameters and requirements.

