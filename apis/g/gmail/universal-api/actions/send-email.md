# Google Mail: Send Email

Sends a Gmail message.

```
POST https://connect.mindcloud.co/v1/universal/gmail/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "alice@example.com, bob@example.com",
  "subject": "Quick update"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gmail/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "alice@example.com, bob@example.com",
    "subject": "Quick update"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | Recipient email address. Use a comma-separated list for multiple recipients. Example: `alice@example.com, bob@example.com`. |
| `subject` | string | yes | Email subject line. Example: `Quick update`. |
| `bodyText` | string | no | Plain-text email body, if both Body Text and Body Email are used, Body Text will be rendered above Body HTML. Example: `Hello,  Just following up...`. |
| `bodyHtml` | string | no | HTML email body, if both Body Text and Body Email are used, Body Text will be rendered above Body HTML. Example: `<p>Hello from MindCloud</p>`. |
| `attachmentFile` | file | no | Optional single attachment file to include with the email. |
| `cc` | string | no | Optional CC recipients. Use a comma-separated list. Example: `manager@example.com`. |
| `bcc` | string | no | Optional BCC recipients. Use a comma-separated list. Example: `audit@example.com`. |
| `from` | string | no | Optional sender header. Must be permitted by Gmail account configuration. Example: `me@example.com`. |
| `replyTo` | string | no | Optional Reply-To address. Example: `replyto@example.com`. |
| `threadId` | string | no | Optional Gmail thread ID to reply in an existing thread. Example: `19c7cd447accadc2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachmentFilename` | string | no | Optional attachment filename override. Defaults to the uploaded file name when available. |
| `attachmentMimeType` | string | no | Optional attachment MIME type override. Defaults to application/octet-stream when unknown. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "labelIds": [
        "string"
      ],
      "threadId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `labelIds[]` | string |  |
| `threadId` | string |  |

## Native endpoint

Through the native Google Mail API, this operation is `POST /messages/send` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

