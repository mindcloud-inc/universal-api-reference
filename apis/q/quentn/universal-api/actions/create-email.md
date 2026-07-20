# Quentn: Create Email



```
POST https://connect.mindcloud.co/v1/universal/quentn/latest/actions/create-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/create-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "MindCloud Stage 2 Test Email",
  "bodyHtml": "<p>Hello from MindCloud</p>",
  "context": "opt_in_mail"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quentn/latest/actions/create-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "MindCloud Stage 2 Test Email",
    "bodyHtml": "<p>Hello from MindCloud</p>",
    "context": "opt_in_mail"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | The email subject line. Example: `MindCloud Stage 2 Test Email`. |
| `bodyHtml` | string | yes | HTML content of the email. Example: `<p>Hello from MindCloud</p>`. |
| `context` | string | yes | Mail context, for example opt_in_mail or webinar_reminder. Example: `opt_in_mail`. |
| `bodyText` | string | no | Optional plain-text email body. Example: `Hello from MindCloud`. |
| `senderId` | number | no | Optional sender id from List Mail Senders. Example: `1`. |

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
| `id` | string |  |

## Native endpoint

Through the native Quentn API, this operation is `POST /mail/add` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email.md) for the provider-specific parameters and requirements.

