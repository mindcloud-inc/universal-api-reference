# OneSuite: Update Invoice

Updates an invoice in OneSuite.

```
PUT https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": "string",
  "company": "string",
  "client.key": "string",
  "clientName": "Ava Chen",
  "clientCompany": "string",
  "description": "string",
  "subTotalPrice": 1,
  "salesTax": 1,
  "totalPrice": 1,
  "dueDate": "2026-05-07T12:00:00.000Z",
  "currency": "string",
  "invoiceNo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": "string",
    "company": "string",
    "client.key": "string",
    "clientName": "Ava Chen",
    "clientCompany": "string",
    "description": "string",
    "subTotalPrice": 1,
    "salesTax": 1,
    "totalPrice": 1,
    "dueDate": "2026-05-07T12:00:00.000Z",
    "currency": "string",
    "invoiceNo": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Your company address |
| `city` | string | no | Your company city |
| `createdDate` | date | no | Invoice create date |
| `email` | string | no | Your company email address |
| `invoiceId` | string | yes | Invoice ID |
| `invoiceItems[]` | array<object> | no | Invoice line items |
| `note` | string | no | Notes for the invoice |
| `phone` | string | no | Your company contact number |
| `postBoxNo` | string | no | Post box number |
| `street` | string | no | Your company street |
| `company` | string | yes | Your company name |
| `client.key` | string | yes | Client ID |
| `clientName` | string | yes | Client display name |
| `clientCompany` | string | yes | Client company name |
| `description` | string | yes | Invoice description |
| `subTotalPrice` | number | yes | Subtotal price |
| `salesTax` | number | yes | Sales tax amount |
| `totalPrice` | number | yes | Total price |
| `dueDate` | date | yes | Invoice due date |
| `currency` | string | yes | Currency code |
| `project.key` | string | no | Project ID |
| `name` | string | no | Invoice name |
| `invoiceNo` | string | yes | Invoice number |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneSuite API returns.

## Native endpoint

Through the native OneSuite API, this operation is `PATCH /v1/invoices/:invoice_id` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

