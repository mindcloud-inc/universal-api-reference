# Maildrip: Send a transactional email with raw data



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-a-transactional-email-with-raw-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-a-transactional-email-with-raw-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-a-transactional-email-with-raw-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailAddress` | string | no |  |
| `subject` | string | no |  |
| `html` | string | no |  |
| `bcc[]` | array<string> | no | List of BCC email addresses Accepts multiple values as an array. |
| `variables` | object | no | Template for mailgun variables for substitution or Mumara for personalization |
| `provider` | string | no | Email service provider to use |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/emails/transaction` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-a-transactional-email-with-raw-data.md) for the provider-specific parameters and requirements.

