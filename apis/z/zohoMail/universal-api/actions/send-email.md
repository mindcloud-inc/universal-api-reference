# Zoho Mail: Send Email

Sends an email through Zoho Mail.

```
POST https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "fromAddress": "gabrielrodrigues.345@zohomail.com",
  "toAddress": "gabrielrodrigues.345@zohomail.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "fromAddress": "gabrielrodrigues.345@zohomail.com",
    "toAddress": "gabrielrodrigues.345@zohomail.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | list<string> | yes | Zoho Mail account ID. |
| `fromAddress` | string | yes | Sender email address. Example: `gabrielrodrigues.345@zohomail.com`. |
| `toAddress` | string | yes | Comma-separated recipient email addresses. Example: `gabrielrodrigues.345@zohomail.com`. |
| `subject` | string | no | Email subject line. Example: `Stage 3 test email`. |
| `content` | string | no | Email body content. Example: `Hello from MindCloud.`. |
| `mailFormat` | list<string> | no | Body format. One of: `html`, `plaintext`. Example: `html`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ccAddress` | string | no | Comma-separated CC recipient email addresses. Example: `teammate@example.com`. |
| `bccAddress` | string | no | Comma-separated BCC recipient email addresses. Example: `auditor@example.com`. |
| `askReceipt` | list<string> | no | Whether to request a read receipt. One of: `no`, `yes`. |
| `encoding` | string | no | Body content encoding. Example: `text/html; charset=UTF-8`. |
| `isSchedule` | boolean | no | Whether to schedule the email instead of sending immediately. |
| `scheduleType` | list<string> | no | Scheduling rule type. One of: `1`, `2`, `3`, `4`, `5`, `6`. |
| `timeZone` | string | no | Time zone to use when scheduling by specific date and time. Example: `America/Sao_Paulo`. |
| `scheduleTime` | string | no | Scheduled send time in Zoho Mail format. Example: `03/12/2026 09:00:00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "fromAddress": "string",
      "mailId": "string",
      "messageId": "string",
      "subject": "string",
      "toAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Email body content |
| `fromAddress` | string | From address |
| `mailId` | string | Mail header identifier |
| `messageId` | string | Message identifier |
| `subject` | string | Email subject |
| `toAddress` | string | To address |

## Native endpoint

Through the native Zoho Mail API, this operation is `POST /accounts/:accountId/messages` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

