# Maildrip: Send email via Mumara



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-email-via-mumara
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-email-via-mumara" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recipient": "string",
  "subject": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-email-via-mumara', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recipient": "string",
    "subject": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipient` | string | yes | Recipient email address |
| `subject` | string | yes | Email subject |
| `body` | string | yes | HTML or plain text email body |
| `fromName` | string | no | Sender name (optional, falls back to user settings) |
| `fromEmail` | string | no | Sender email (optional, uses domain/node settings) |
| `replyTo` | string | no | Reply-to address (optional) |
| `nodeId` | string | no | Optional - Specific sending node ID (DynamoDB UUID) |
| `domainId` | string | no | Optional - Specific domain ID (DynamoDB UUID) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/mumara/send-email` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email-via-mumara.md) for the provider-specific parameters and requirements.

