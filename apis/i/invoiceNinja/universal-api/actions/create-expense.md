# Invoice Ninja: Create Expense



```
POST https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-expense', {
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
| `vendorId` | string | no | The vendor for the expense. |
| `amount` | number | no | Expense amount. |
| `date` | string | no | Expense date. |
| `privateNotes` | string | no | Internal expense notes. |
| `publicNotes` | string | no | Expense description visible on documents. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "archivedAt": 1,
      "categoryId": "string",
      "clientId": "string",
      "createdAt": 1,
      "currencyId": "string",
      "date": "string",
      "documents": [
        {}
      ],
      "eInvoice": {},
      "entityType": "string",
      "exchangeRate": 1,
      "id": "string",
      "isDeleted": true,
      "number": "string",
      "paymentTypeId": "string",
      "privateNotes": "string",
      "publicNotes": "string",
      "transactionReference": "string",
      "updatedAt": 1,
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `archivedAt` | number |  |
| `categoryId` | string |  |
| `clientId` | string |  |
| `createdAt` | number |  |
| `currencyId` | string |  |
| `date` | string |  |
| `documents` | array<object> |  |
| `eInvoice` | object |  |
| `entityType` | string |  |
| `exchangeRate` | number |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `number` | string |  |
| `paymentTypeId` | string |  |
| `privateNotes` | string |  |
| `publicNotes` | string |  |
| `transactionReference` | string |  |
| `updatedAt` | number |  |
| `vendorId` | string |  |

## Native endpoint

Through the native Invoice Ninja API, this operation is `POST /expenses` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense.md) for the provider-specific parameters and requirements.

