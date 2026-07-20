# Clockify: Change Invoice Status

Updates an invoice status in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/change-invoice-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/change-invoice-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "invoiceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/change-invoice-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "invoiceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `invoiceId` | string<string> | yes |  |
| `invoiceStatus` | list<string> | no | One of: `OVERDUE`, `PAID`, `PARTIALLY_PAID`, `SENT`, `UNSENT`, `VOID`. Example: `ACTIVE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "balance": 1,
      "billFrom": "string",
      "calculationType": "string",
      "clientAddress": "string",
      "clientId": "string",
      "clientName": "Ava Chen",
      "companyId": "string",
      "containsImportedExpenses": true,
      "containsImportedTimes": true,
      "currency": "string",
      "discount": 1,
      "discountAmount": 1,
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "issuedDate": "2026-05-07T12:00:00.000Z",
      "items": [
        [
          {}
        ]
      ],
      "note": "string",
      "number": "string",
      "paid": 1,
      "status": "string",
      "subject": "string",
      "subtotal": 1,
      "tax": 1,
      "tax2": 1,
      "tax2Amount": 1,
      "taxAmount": 1,
      "taxType": "string",
      "userId": "string",
      "visibleZeroFields": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `balance` | number |  |
| `billFrom` | string |  |
| `calculationType` | string |  |
| `clientAddress` | string |  |
| `clientId` | string |  |
| `clientName` | string |  |
| `companyId` | string |  |
| `containsImportedExpenses` | boolean |  |
| `containsImportedTimes` | boolean |  |
| `currency` | string |  |
| `discount` | number |  |
| `discountAmount` | number |  |
| `dueDate` | date |  |
| `id` | string |  |
| `issuedDate` | date |  |
| `items[]` | array<object> |  |
| `items[].amount` | number |  |
| `items[].applyTaxes` | string |  |
| `items[].description` | string |  |
| `items[].itemType` | string |  |
| `items[].order` | number |  |
| `items[].quantity` | number |  |
| `items[].timeEntryIds[]` | array<string> |  |
| `items[].unitPrice` | number |  |
| `note` | string |  |
| `number` | string |  |
| `paid` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `subtotal` | number |  |
| `tax` | number |  |
| `tax2` | number |  |
| `tax2Amount` | number |  |
| `taxAmount` | number |  |
| `taxType` | string |  |
| `userId` | string |  |
| `visibleZeroFields` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `PATCH workspaces/:workspaceId/invoices/:invoiceId/status` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-invoice-status.md) for the provider-specific parameters and requirements.

