# OneSuite: Create Invoice

Creates an invoice in OneSuite.

```
POST https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `company` | string | yes | Your company name |
| `createdDate` | date | no | Invoice create date |
| `email` | string | no | Your company email address |
| `invoiceItems[]` | array<object> | no | Invoice line items |
| `note` | string | no | Notes for the invoice |
| `phone` | string | no | Your company contact number |
| `postBoxNo` | string | no | Post box number |
| `street` | string | no | Your company street |
| `client.key` | string | yes | Client ID |
| `clientName` | string | yes | Client display name |
| `clientCompany` | string | yes | Client company name |
| `description` | string | yes | Invoice description |
| `subTotalPrice` | number | yes | Subtotal price |
| `salesTax` | number | yes | Sales tax amount |
| `totalPrice` | number | yes | Total price |
| `dueDate` | date | yes | Invoice due date |
| `currency` | string | yes | Currency code |
| `invoiceNo` | string | yes | Invoice number |
| `project.key` | string | no | Project ID |
| `name` | string | no | Invoice name |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneSuite API returns.

## Native endpoint

Through the native OneSuite API, this operation is `POST /v1/invoices` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

