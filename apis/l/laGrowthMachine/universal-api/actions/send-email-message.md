# LaGrowthMachine: Send Email Message

Sends an email message to a lead in LaGrowthMachine.

```
POST https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/send-email-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/send-email-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identityId": "string",
  "message.html": "string",
  "message.text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/send-email-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identityId": "string",
    "message.html": "string",
    "message.text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bcc` | string | no | Comma-separated BCC recipients. |
| `cc` | string | no | Comma-separated CC recipients. |
| `identityId` | string | yes | Email identity that sends the message. |
| `leadEmail` | string | no | Target lead email. Provide either Lead ID or Lead Email. |
| `leadId` | string | no | Target lead ID. Provide either Lead ID or Lead Email. |
| `message.html` | string | yes | HTML version of the email body. |
| `message.text` | string | yes | Plain-text version of the email body. |
| `replyInLastThread` | boolean | no | Whether to reply in the latest thread. |
| `replyToMessageId` | string | no | Specific message ID to reply to. |
| `subject` | string | no | Email subject when not replying in thread. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lead": {
        "companyName": "Ava Chen",
        "firstname": "Ava",
        "id": "string",
        "lastMessageSentAt": 1,
        "lastname": "Chen",
        "linkedinUrl": "https://example.com",
        "proEmail": "ava@example.com"
      },
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lead.companyName` | string | Lead company name. |
| `lead.firstname` | string | Lead first name. |
| `lead.id` | string | Lead identifier. |
| `lead.lastMessageSentAt` | number | Timestamp of the latest sent message. |
| `lead.lastname` | string | Lead last name. |
| `lead.linkedinUrl` | string | Lead LinkedIn profile URL. |
| `lead.proEmail` | string | Lead professional email. |
| `statusCode` | number | Provider status code returned after sending the email message. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `POST /inbox/email` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email-message.md) for the provider-specific parameters and requirements.

