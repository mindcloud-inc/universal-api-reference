# MailerSend: Update Sender Identity



```
PUT https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/update-sender-identity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/update-sender-identity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/update-sender-identity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identityId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identityId` | string | yes | ID of the sender identity to update. |
| `name` | string | no | Updated display name for the sender identity. |
| `replyToEmail` | string | no | Updated reply-to email for the sender identity. |
| `replyToName` | string | no | Updated reply-to display name for the sender identity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addNote": true,
      "domain": {},
      "email": "ava@example.com",
      "id": "string",
      "isVerified": true,
      "name": "Ava Chen",
      "personalNote": "string",
      "replyToEmail": "ava@example.com",
      "replyToName": "Ava Chen",
      "resends": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addNote` | boolean | Whether a personal verification note is enabled. |
| `domain` | object | Domain metadata linked to the sender identity. |
| `email` | string | Sender identity email address. |
| `id` | string | MailerSend sender identity ID. |
| `isVerified` | boolean | Whether the sender identity is verified. |
| `name` | string | Sender identity display name. |
| `personalNote` | string | Personal verification note content when configured. |
| `replyToEmail` | string | Reply-to email address when configured. |
| `replyToName` | string | Reply-to display name when configured. |
| `resends` | number | Number of verification resend attempts. |

## Native endpoint

Through the native MailerSend API, this operation is `PUT /identities/:identity_id` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sender-identity.md) for the provider-specific parameters and requirements.

