# Moxie: Create Invoice

Creates a new invoice in Moxie.

```
POST https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientName": "Ava Chen",
  "items": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientName": "Ava Chen",
    "items": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientName` | string | yes | Existing client name for the invoice. |
| `dueDate` | date | no | Invoice due date. |
| `templateName` | string | no | Invoice template name. |
| `invoiceNumber` | string | no | Custom invoice number. |
| `taxRate` | number | no | Invoice tax rate percentage. |
| `discountPercent` | number | no | Invoice discount percentage. |
| `paymentInstructions` | string | no | Payment instructions shown on the invoice. |
| `items` | list<object> | yes | List of invoice line items. |
| `sendTo` | object | no | Recipient object for sending the invoice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "amountDue": 1,
      "clientId": "string",
      "clientInfo": {},
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateDue": "2026-05-07T12:00:00.000Z",
      "datePaid": "2026-05-07T12:00:00.000Z",
      "dateSent": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "integrationKeys": {},
      "invoiceNumber": 1,
      "invoiceNumberFormatted": "string",
      "invoiceType": "string",
      "payments": [
        {}
      ],
      "paymentTotal": 1,
      "status": "string",
      "total": 1,
      "viewOnlineUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `amountDue` | number |  |
| `clientId` | string |  |
| `clientInfo` | object |  |
| `currency` | string |  |
| `dateCreated` | date |  |
| `dateDue` | date |  |
| `datePaid` | date |  |
| `dateSent` | date |  |
| `id` | string |  |
| `integrationKeys` | object |  |
| `invoiceNumber` | number |  |
| `invoiceNumberFormatted` | string |  |
| `invoiceType` | string |  |
| `payments` | array<object> |  |
| `paymentTotal` | number |  |
| `status` | string |  |
| `total` | number |  |
| `viewOnlineUrl` | string |  |

## Native endpoint

Through the native Moxie API, this operation is `POST /action/invoices/create` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

