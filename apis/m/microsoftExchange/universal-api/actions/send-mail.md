# Microsoft Exchange: Send Mail

Sends an email from Microsoft Exchange.

```
POST https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/send-mail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Exchange `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/send-mail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/send-mail', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message.toRecipients[].emailAddress.address` | string | no | The recipient email address. Example: `jamie@mindcloud.co`. |
| `message.subject` | string | no | The email subject line. Example: `MindCloud Exchange send test`. |
| `message.body.content` | string | no | The text content of the email body. Example: `This is a test email sent from the MindCloud Microsoft Exchange app.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Exchange API returns.

## Native endpoint

Through the native Microsoft Exchange API, this operation is `POST /v1.0/me/sendMail` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-mail.md) for the provider-specific parameters and requirements.

