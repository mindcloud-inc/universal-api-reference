# boomApp Connect: Send Email

Creates an email message in boomApp Connect.

```
POST https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a boomApp Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email_subject": "Email subject",
  "message_content": "Email body",
  "email_address[]": "test@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email_subject": "Email subject",
    "message_content": "Email body",
    "email_address[]": "test@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | no | Sender ID displayed in the recipient inbox. |
| `email_subject` | string | yes | Email subject displayed in the recipient inbox. Required for successful runtime submission. Example: `Email subject`. |
| `message_content` | string | yes | Email body content. Required for successful runtime submission. Example: `Email body`. |
| `email_address[]` | array<string> | yes | Recipient email addresses. Required for successful runtime submission. Example: `test@example.com`. |
| `validity_period` | number | no | Validity period in days. |
| `open_ticket` | boolean | no | Set true to enable an open ticket for multiple responses. |
| `email_responses` | string | no | Email address to forward message responses. |
| `push_responses` | string | no | Callback URL for posted responses. |
| `unique_identifier` | string | no | Customer-side dedupe identifier. |
| `campaign_name` | string | no | Optional campaign grouping name. |
| `custom_parameter` | string | no | Optional custom reference value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1,
      "transactions": {
        "boomerangId": "string",
        "emailAddress": "ava@example.com",
        "partsPerMessage": 1,
        "transactionId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Response message. |
| `status` | number | Response status code. |
| `transactions` | array<object> | Outbound email transaction results. |
| `transactions.boomerangId` | string | Boomerang message ID. |
| `transactions.emailAddress` | string | Recipient email address. |
| `transactions.partsPerMessage` | number | Parts per message. |
| `transactions.transactionId` | string | Boomerang transaction ID. |

## Native endpoint

Through the native boomApp Connect API, this operation is `POST /v1/flat/email` (base URL `https://direct-api.apps.boomcomms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

