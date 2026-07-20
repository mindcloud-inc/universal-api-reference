# Refrens: Send Invoice Email



```
POST https://connect.mindcloud.co/v1/universal/refrens/latest/actions/send-invoice-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refrens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/send-invoice-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceID": "string",
  "to": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refrens/latest/actions/send-invoice-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceID": "string",
    "to": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceID` | string | yes |  |
| `to` | object | yes | Recipient object with email and optional name. |
| `cc[]` | array<object> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | object | no | Optional sender object. Refrens requires the sender email to be connected in Refrens before use. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "cc": [
        {}
      ],
      "emailType": "ava@example.com",
      "from": {},
      "isExpenditureEmail": true,
      "subject": "string",
      "to": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `cc` | array<object> |  |
| `emailType` | string |  |
| `from` | object |  |
| `isExpenditureEmail` | boolean |  |
| `subject` | string |  |
| `to` | object |  |

## Native endpoint

Through the native Refrens API, this operation is `POST /businesses/:urlKey/invoices/:invoiceID/email` (base URL `https://api.refrens.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-invoice-email.md) for the provider-specific parameters and requirements.

