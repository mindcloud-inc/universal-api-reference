# MailoPost: Send Email Message

Sends an email message in MailoPost.

```
POST https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/send-email-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/send-email-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromEmail": "ava@example.com",
  "to": "string",
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/send-email-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromEmail": "ava@example.com",
    "to": "string",
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromEmail` | string | yes | Sender email address. |
| `to` | string | yes | Recipient email address. |
| `subject` | string | yes | Email subject line. |
| `text` | string | no | Plain-text message body. Provide text or html. |
| `html` | string | no | HTML message body. Provide html or text. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromName` | string | no | Sender display name. |
| `payment` | string | no | Billing mode for the message. Example: `subscriber_priority`. |
| `smtpHeaders` | object | no | Additional SMTP headers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        "string"
      ],
      "events": {
        "open": 1,
        "spam": 1,
        "unsubscribe": 1
      },
      "from_email": "ava@example.com",
      "from_name": "Ava Chen",
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
| `attachments[]` | string |  |
| `events.open` | number |  |
| `events.spam` | number |  |
| `events.unsubscribe` | number |  |
| `from_email` | string |  |
| `from_name` | string |  |
| `html` | string |  |
| `id` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `text` | string |  |
| `to` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `POST /email/messages` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email-message.md) for the provider-specific parameters and requirements.

