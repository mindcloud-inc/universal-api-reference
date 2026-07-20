# MailSlurp Email Plugin: Reply To Email

Replies to an email in MailSlurp.

```
POST https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/reply-to-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailSlurp Email Plugin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/reply-to-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailSlurpEmailPlugin/latest/actions/reply-to-email', {
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
| `emailId` | string | no | The MailSlurp email ID to reply to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "from": "string",
      "id": "string",
      "inboxId": "string",
      "sentAt": "string",
      "subject": "string",
      "to": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `from` | string |  |
| `id` | string |  |
| `inboxId` | string |  |
| `sentAt` | string |  |
| `subject` | string |  |
| `to` | array<string> |  |

## Native endpoint

Through the native MailSlurp Email Plugin API, this operation is `PUT /emails/:emailId` (base URL `https://api.mailslurp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reply-to-email.md) for the provider-specific parameters and requirements.

