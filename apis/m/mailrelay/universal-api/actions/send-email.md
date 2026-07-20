# Mailrelay: Send Email

Sends an email to one or more recipients through Mailrelay.

```
POST https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": {},
  "from.email": "apps@mindcloud.co",
  "subject": "Welcome to MindCloud",
  "to[]": [
    "string"
  ],
  "to[].email": "recipient@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": {},
    "from.email": "apps@mindcloud.co",
    "subject": "Welcome to MindCloud",
    "to[]": ["string"],
    "to[].email": "recipient@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | object | yes | From header object. |
| `from.email` | string | yes | From email address. Example: `apps@mindcloud.co`. |
| `from.name` | string | no | From display name. |
| `htmlPart` | string | no | HTML email content. Example: `<html><body><p>Hello!</p></body></html>`. |
| `subject` | string | yes | Email subject. Example: `Welcome to MindCloud`. |
| `textPart` | string | no | Plain-text email content. Example: `Hello!`. |
| `textPartAuto` | boolean | no | Automatically generate plain-text content from HTML. Example: `true`. |
| `to[]` | array | yes | Recipient list. |
| `to[].email` | string | yes | Recipient email address. Example: `recipient@example.com`. |
| `to[].name` | string | no | Recipient display name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "subscriberId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | number |  |
| `subscriberId` | number |  |

## Native endpoint

Through the native Mailrelay API, this operation is `POST send_emails` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

