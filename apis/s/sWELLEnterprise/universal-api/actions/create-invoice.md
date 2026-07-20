# SWELLEnterprise: Create Invoice

Creates a new invoice in SWELLEnterprise.

```
POST https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceNumber": "string",
  "status": "string",
  "invoiceDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceNumber": "string",
    "status": "string",
    "invoiceDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceNumber` | string | yes | The invoice number. |
| `status` | string | yes | The invoice status. |
| `contactId` | number | no | The contact ID. |
| `invoiceDate` | date | yes | The invoice date. |
| `companyId` | number | no | The company ID. |
| `dueDate` | date | no | The due date. |
| `subtotal` | number | no | The subtotal. |
| `taxRate` | number | no | The tax rate percentage. |
| `total` | number | no | The total. |
| `currency` | string | no | The currency code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "companyId": 1,
        "contactId": 1,
        "currency": "string",
        "dueDate": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "invoiceDate": "2026-05-07T12:00:00.000Z",
        "invoiceNumber": "string",
        "status": "string",
        "total": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.companyId` | number | The linked company ID. |
| `data.contactId` | number | The linked contact ID. |
| `data.currency` | string | The currency code. |
| `data.dueDate` | date | The due date. |
| `data.id` | number | The invoice ID. |
| `data.invoiceDate` | date | The invoice date. |
| `data.invoiceNumber` | string | The invoice number. |
| `data.status` | string | The invoice status. |
| `data.total` | string | The invoice total. |
| `message` | string | Success message. |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `POST /finance/invoices` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

