# Engage: Send Email

Sends a transactional email through Engage.

```
POST https://connect.mindcloud.co/v1/universal/engage/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Engage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/engage/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "from.email": "ava@example.com",
  "from.name": "Ava Chen",
  "to[]": [
    "string"
  ],
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/engage/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "from.email": "ava@example.com",
    "from.name": "Ava Chen",
    "to[]": ["string"],
    "html": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bcc[]` | array<string> | no | Email addresses for the blind carbon copy field. |
| `cc[]` | array<string> | no | Email addresses for the carbon copy field. |
| `replyTo` | string | no | Custom address that replies should go to. |
| `subject` | string | yes | The email subject. |
| `template` | string | no | Template name or identifier for a saved email template. |
| `templateVariables` | object | no | Variables for the selected email template. |
| `text` | string | no | Alternative text version of the email content. |
| `trackClicks` | boolean | no | Set to true to enable click tracking. |
| `trackOpens` | boolean | no | Set to true to enable open tracking. |
| `from.email` | string | yes | Sender email address. |
| `from.name` | string | yes | Sender name. |
| `to[]` | array<string> | yes | Recipient email address or addresses. |
| `html` | string | yes | HTML content of the email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Identifier of the sent transactional email message. |

## Native endpoint

Through the native Engage API, this operation is `POST /send/email` (base URL `https://api.engage.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

