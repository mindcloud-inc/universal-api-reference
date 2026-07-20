# Zoho Invoice: Email Invoice

Emails an invoice from Zoho Invoice.

```
POST https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/email-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/email-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "invoiceId": "string",
  "toMailIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/email-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "invoiceId": "string",
    "toMailIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | list<string> | yes | ID of the organization header X-com-zoho-invoice-organizationid. |
| `invoiceId` | string | yes | Unique identifier of the invoice. |
| `sendFromOrgEmailId` | boolean | no | Boolean to trigger the email from the organization's email address. |
| `toMailIds[]` | array<string> | yes | Array of email addresses of the recipients. |
| `ccMailIds[]` | array<string> | no | Array of email addresses of the recipients to be CC'd. |
| `subject` | string | no | The subject of the mail. |
| `body` | string | no | The body content of the mail. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendCustomerStatement` | boolean | no | Send customer statement PDF with the email. |
| `sendAttachment` | boolean | no | Send the invoice attachment with the email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "isFirstEmail": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `isFirstEmail` | boolean |  |
| `message` | string |  |

## Native endpoint

Through the native Zoho Invoice API, this operation is `POST /invoices/:invoice_id/email` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-invoice.md) for the provider-specific parameters and requirements.

