# Zoho Mail: Save Draft

Creates a draft email in Zoho Mail.

```
POST https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/save-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/save-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "fromAddress": "gabrielrodrigues.345@zohomail.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/save-draft', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "fromAddress": "gabrielrodrigues.345@zohomail.com"
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
| `toAddress` | string | no | Comma-separated recipient email addresses. Example: `gabrielrodrigues.345@zohomail.com`. |
| `subject` | string | no | Draft subject line. Example: `Draft subject`. |
| `content` | string | no | Draft body content. Example: `Draft content`. |
| `mailFormat` | list<string> | no | Body format. One of: `html`, `plaintext`. Example: `html`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ccAddress` | string | no | Comma-separated CC recipient email addresses. Example: `teammate@example.com`. |
| `bccAddress` | string | no | Comma-separated BCC recipient email addresses. Example: `auditor@example.com`. |
| `askReceipt` | list<string> | no | Whether to request a read receipt when the draft is sent. One of: `no`, `yes`. |
| `encoding` | string | no | Body content encoding. Example: `text/html; charset=UTF-8`. |
| `inReplyTo` | string | no | Original message reference for threading. Example: `<message-id@example.com>`. |
| `refHeader` | string | no | Reference headers for threading. Example: `<msg1@example.com> <msg2@example.com>`. |

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
      "mode": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Draft content |
| `fromAddress` | string | From address |
| `mailId` | string | Mail header identifier |
| `messageId` | string | Message identifier |
| `mode` | string | Message mode |
| `subject` | string | Email subject |

## Native endpoint

Through the native Zoho Mail API, this operation is `POST /accounts/:accountId/messages` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-draft.md) for the provider-specific parameters and requirements.

