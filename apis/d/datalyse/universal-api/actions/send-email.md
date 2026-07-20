# Datalyse: Send Email

Sends an email from Datalyse.

```
POST https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datalyse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string",
  "subject": "string",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "string",
    "subject": "string",
    "to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bcc` | string | no | BCC recipients (optional) |
| `cc` | string | no | CC recipients (optional) |
| `html` | string | yes | Email body in HTML |
| `leadId` | string | no | Associate email with a contact ID (optional) |
| `opportunityId` | string | no | Associate email with an opportunity ID (optional) |
| `signatureId` | string | no | Append this signature to the email (optional, get from signatures/get) |
| `subject` | string | yes | Email subject |
| `to` | string | yes | Recipient email address |
| `tracking` | string | no | Enable open tracking, set to "y" (optional) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | API response status |

## Native endpoint

Through the native Datalyse API, this operation is `POST /api/1.0/emails/send.json` (base URL `https://api.datalyse.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

