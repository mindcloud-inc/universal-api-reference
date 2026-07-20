# D7 Networks: Send WhatsApp Text Message

Sends a WhatsApp text message with D7 Networks.

```
POST https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/send-whats-app-text-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/send-whats-app-text-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[].originator": "string",
  "messages[].recipients[].recipient": "string",
  "messages[].content.text.body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/d7Networks/latest/actions/send-whats-app-text-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[].originator": "string",
    "messages[].recipients[].recipient": "string",
    "messages[].content.text.body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[].originator` | string | yes | WhatsApp Business sender number or configured originator. |
| `messages[].recipients[].recipient` | string | yes | Recipient WhatsApp number with country code. |
| `messages[].content.text.body` | string | yes | Text body to send. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[].content.text.preview_url` | boolean | no | Whether WhatsApp should render link previews. Default: `false`. |

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

Through the native D7 Networks API, this operation is `POST /whatsapp/v2/send` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-whats-app-text-message.md) for the provider-specific parameters and requirements.

