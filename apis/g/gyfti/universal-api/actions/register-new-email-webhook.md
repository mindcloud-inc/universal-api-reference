# gyfti: Register New Email Webhook

Registers a new email webhook in gyfti.

```
POST https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/register-new-email-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a gyfti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/register-new-email-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hookUrl": "https://example.com",
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/register-new-email-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hookUrl": "https://example.com",
    "user": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hookUrl` | string | yes | Destination URL that gyfti should call when a new email event occurs. |
| `user` | string | yes | gyfti user email associated with the webhook registration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Campaign Name": "Ava Chen",
      "Email Status": "ava@example.com",
      "Message": "string",
      "Recipient Email": "ava@example.com",
      "Recipient First Name": "Ava",
      "Recipient Last Name": "Chen",
      "Send date": "2026-05-07T12:00:00.000Z",
      "Sender Email": "ava@example.com",
      "Sender First Name": "Ava",
      "Sender Last Name": "Chen",
      "Subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Campaign Name` | string |  |
| `Email Status` | string |  |
| `Message` | string |  |
| `Recipient Email` | string |  |
| `Recipient First Name` | string |  |
| `Recipient Last Name` | string |  |
| `Send date` | date |  |
| `Sender Email` | string |  |
| `Sender First Name` | string |  |
| `Sender Last Name` | string |  |
| `Subject` | string |  |

## Native endpoint

Through the native gyfti API, this operation is `POST /wf/new_hook_email/` (base URL `https://app.gyfti.fr/api/1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-new-email-webhook.md) for the provider-specific parameters and requirements.

