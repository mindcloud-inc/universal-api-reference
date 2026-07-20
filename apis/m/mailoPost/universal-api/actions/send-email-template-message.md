# MailoPost: Send Email Template Message

Sends an email from a MailoPost template.

```
POST https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/send-email-template-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/send-email-template-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/send-email-template-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | MailoPost template identifier. |
| `to` | string | yes | Recipient email address. |
| `params` | object | no | Template substitution values. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payment` | string | no | Billing mode for the template message. Example: `subscriber_priority`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string",
      "id": 1,
      "status": "string",
      "subject": "string",
      "text": "string",
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string |  |
| `id` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `text` | string |  |
| `to` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `POST /email/templates/:template_id/messages` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email-template-message.md) for the provider-specific parameters and requirements.

