# Bexio: Send Invoice

Sends an invoice from Bexio by email.

```
PUT https://connect.mindcloud.co/v1/universal/bexio/latest/actions/send-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/send-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": 1,
  "recipientEmail": "ava@example.com",
  "subject": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bexio/latest/actions/send-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": 1,
    "recipientEmail": "ava@example.com",
    "subject": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | number | yes | The ID of the invoice. |
| `recipientEmail` | string | yes | During the trial period, the recipient is limited to the email address associated to the access token provided. |
| `subject` | string | yes | The email subject. |
| `message` | string | yes | The email message. The placeholder [Network Link] must be part of the text. |
| `markAsOpen` | boolean | no | Mark the invoice as open when sending the email. |
| `attachPdf` | boolean | no | Attach the PDF directly to the email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Bexio API, this operation is `POST /2.0/kb_invoice/:invoice_id/send` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-invoice.md) for the provider-specific parameters and requirements.

