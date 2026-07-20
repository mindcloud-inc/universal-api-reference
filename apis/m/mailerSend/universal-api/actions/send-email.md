# MailerSend: Send Email



```
POST https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from.email": "ava@example.com",
  "subject": "string",
  "text": "string",
  "to[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from.email": "ava@example.com",
    "subject": "string",
    "text": "string",
    "to[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from.email` | string | yes | Verified sender email address for this message. |
| `from.name` | string | no | Display name for the sender. |
| `html` | string | no | HTML body of the email. |
| `subject` | string | yes | Email subject line. |
| `text` | string | yes | Plain-text body of the email. |
| `to[].email` | string | yes | Email address for one recipient. |
| `to[].name` | string | no | Display name for one recipient. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MailerSend API returns.

## Native endpoint

Through the native MailerSend API, this operation is `POST /email` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

