# Outlook: Send Mail

Sends a new email from Outlook.

```
POST https://connect.mindcloud.co/v1/universal/outlook/latest/actions/send-mail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outlook/latest/actions/send-mail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "Quarterly update",
  "bodyContent": "Write the email body here.",
  "bodyContentType": "Text",
  "toRecipients": "person@example.com, other@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outlook/latest/actions/send-mail', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "Quarterly update",
    "bodyContent": "Write the email body here.",
    "bodyContentType": "Text",
    "toRecipients": "person@example.com, other@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | Email subject. Example: `Quarterly update`. |
| `bodyContent` | string | yes | Email body content. Example: `Write the email body here.`. |
| `bodyContentType` | list | yes | Email body content type: Text or HTML. One of: `0`, `1`. Default: `Text`. |
| `toRecipients` | string<object> | yes | Comma-separated email addresses to send to. Example: person@example.com, other@example.com Example: `person@example.com, other@example.com`. |
| `saveToSentItems` | boolean | no | Whether Microsoft should save the sent message to Sent Items. Defaults to true. Default: `true`. |
| `ccRecipients` | string | no | Optional CC recipients. Use a comma separated list. Example: `manager@example.com`. |
| `bccRecipients` | string | no | Optional BCC recipients. Use a comma separated list. Example: `audit@example.com`. |
| `attachmentFile` | file | no | Optional single attachment file to include with the email. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachmentFilename` | string | no | Optional attachment filename override. Defaults to the uploaded file name when available. |
| `attachmentMimeType` | string | no | Optional attachment MIME type override. Defaults to application/octet-stream when unknown. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Outlook API returns.

## Native endpoint

Through the native Outlook API, this operation is `POST /me/sendMail` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-mail.md) for the provider-specific parameters and requirements.

