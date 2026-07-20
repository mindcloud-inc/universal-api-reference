# Clockify: Get Invoice

Retrieves a specific invoice from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-invoice?connectionId=$CONNECTION_ID&workspaceId=string&invoiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "invoiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-invoice?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `invoiceId` | string<string> | yes |  |

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

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/invoices/:invoiceId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

