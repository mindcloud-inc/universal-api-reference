# D7 Messaging: Send WhatsApp Custom Template Message

Sends a WhatsApp custom template message through D7 Messaging.

```
POST https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/send-whats-app-custom-template-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/send-whats-app-custom-template-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[0].originator": "string",
  "messages[0].recipients[0].recipient": "string",
  "messages[0].content.template.template_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/send-whats-app-custom-template-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[0].originator": "string",
    "messages[0].recipients[0].recipient": "string",
    "messages[0].content.template.template_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[0].originator` | string | yes | Registered WhatsApp sender phone number. |
| `messages[0].recipients[0].recipient` | string | yes | Recipient mobile number in E.164 format including country code. |
| `messages[0].content.template.template_id` | string | yes | Approved WhatsApp template identifier. |
| `messages[0].content.template.language` | string | no | Language code configured for the template. Default: `en`. |
| `messages[0].report_url` | string | no | Webhook URL to receive delivery reports for this message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "request_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `request_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native D7 Messaging API, this operation is `POST /whatsapp/v2/send` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-whats-app-custom-template-message.md) for the provider-specific parameters and requirements.

