# LaGrowthMachine: Send LinkedIn Message

Sends a LinkedIn message to a lead in LaGrowthMachine.

```
POST https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/send-linked-in-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/send-linked-in-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identityId": "string",
  "memberId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/send-linked-in-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identityId": "string",
    "memberId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audioUrl` | string | no | Direct download URL to an MP3 voice message. Provide either audio URL or message. |
| `identityId` | string | yes | Identity ID used to send the LinkedIn message. |
| `leadId` | string | no | Target lead ID. Provide either Lead ID or LinkedIn URL. |
| `linkedinUrl` | string | no | Target lead LinkedIn URL. Provide either Lead ID or LinkedIn URL. |
| `memberId` | string | yes | Member ID associated with the sender. Required by the provider. |
| `message` | string | no | LinkedIn message text. Provide either message or audio URL. |

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
| `statusCode` | number | Provider status code returned after sending the LinkedIn message. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `POST /inbox/linkedin` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-linked-in-message.md) for the provider-specific parameters and requirements.

