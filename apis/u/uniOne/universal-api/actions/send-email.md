# UniOne: Send Email

Sends an email message through UniOne.

```
POST https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message.recipients[].email": "apps@mindcloud.co",
  "message.subject": "MindCloud Send Test",
  "message.body.html": "<p>Hello from MindCloud</p>",
  "message.fromEmail": "no-reply@mindcloud.co",
  "message.fromName": "MindCloud"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message.recipients[].email": "apps@mindcloud.co",
    "message.subject": "MindCloud Send Test",
    "message.body.html": "<p>Hello from MindCloud</p>",
    "message.fromEmail": "no-reply@mindcloud.co",
    "message.fromName": "MindCloud"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message.recipients[].email` | string | yes | Recipient email address. Example: `apps@mindcloud.co`. |
| `message.subject` | string | yes | Email subject. Example: `MindCloud Send Test`. |
| `message.body.html` | string | yes | HTML body content. Example: `<p>Hello from MindCloud</p>`. |
| `message.body.plaintext` | string | no | Plaintext fallback body. Example: `Hello from MindCloud`. |
| `message.fromEmail` | string | yes | Sender email address. Example: `no-reply@mindcloud.co`. |
| `message.fromName` | string | yes | Sender name. Example: `MindCloud`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UniOne API returns.

## Native endpoint

Through the native UniOne API, this operation is `POST email/send.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

