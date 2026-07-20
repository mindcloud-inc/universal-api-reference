# DitLead: Create Mailbox



```
POST https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/create-mailbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/create-mailbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "imap": {},
  "lastName": "Chen",
  "smtp": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/create-mailbox', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "imap": {},
    "lastName": "Chen",
    "smtp": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no |  |
| `firstName` | string | yes | Sender first name. |
| `imap` | object | yes | IMAP credentials object. |
| `imap.host` | string | no |  |
| `imap.password` | string | no |  |
| `imap.port` | string | no |  |
| `imap.username` | string | no |  |
| `lastName` | string | no |  |
| `lastName` | string | yes | Sender last name. |
| `smtp` | object | yes | SMTP credentials object. |
| `smtp.emailAddress` | string | no |  |
| `smtp.host` | string | no |  |
| `smtp.password` | string | no |  |
| `smtp.port` | string | no |  |
| `smtp.secure` | boolean | no |  |
| `smtp.username` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": [
        "string"
      ],
      "eventId": [
        "string"
      ],
      "success": true,
      "updatedAt": [
        "string"
      ],
      "url": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | array<string> |  |
| `eventId` | array<string> |  |
| `success` | boolean |  |
| `updatedAt` | array<string> |  |
| `url` | array<string> |  |

## Native endpoint

Through the native DitLead API, this operation is `POST /v1/mailbox` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mailbox.md) for the provider-specific parameters and requirements.

