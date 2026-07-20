# Microsoft 365 Outlook: Send Mail

Sends a new message from Microsoft 365 Outlook.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/send-mail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/send-mail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "MindCloud Microsoft 365 Outlook send test",
  "bodyContent": "This is a test email sent from the MindCloud Microsoft 365 Outlook app.",
  "bodyContentType": "Text",
  "toRecipients": "jamie@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/send-mail', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "MindCloud Microsoft 365 Outlook send test",
    "bodyContent": "This is a test email sent from the MindCloud Microsoft 365 Outlook app.",
    "bodyContentType": "Text",
    "toRecipients": "jamie@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | Email subject. Example: `MindCloud Microsoft 365 Outlook send test`. |
| `bodyContent` | string | yes | Email body content. Example: `This is a test email sent from the MindCloud Microsoft 365 Outlook app.`. |
| `toRecipients` | string | yes | Comma-separated email addresses to send to. Example: person@example.com, other@example.com Example: `jamie@mindcloud.co`. |
| `saveToSentItems` | boolean | no | Whether Microsoft should save the sent message to Sent Items. Defaults to true. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bodyContentType` | list | yes | Email body content type: Text or HTML. One of: `0`, `1`. Default: `Text`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft 365 Outlook API returns.

## Native endpoint

Through the native Microsoft 365 Outlook API, this operation is `POST /v1.0/me/sendMail` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-mail.md) for the provider-specific parameters and requirements.

