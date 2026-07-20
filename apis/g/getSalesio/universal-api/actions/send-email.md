# GetSales.io: Send Email



```
POST https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/send-email', {
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
| `senderProfileUuid` | string | no | Sender profile UUID. |
| `leadUuid` | string | no | Contact UUID. |
| `fromName` | string | no | Sender display name. Example: `John Doe`. |
| `fromEmail` | string | no | Sender email address. Example: `sender@example.com`. |
| `toName` | string | no | Recipient display name. Example: `Jane Smith`. |
| `toEmail` | string | no | Recipient email address. Example: `jane@example.com`. |
| `subject` | string | no | Email subject. Example: `Quick hello`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailBodyDomain": {},
      "emailDomain": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailBodyDomain` | object |  |
| `emailDomain` | object |  |

## Native endpoint

Through the native GetSales.io API, this operation is `POST /emails/api/emails/send-email` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

