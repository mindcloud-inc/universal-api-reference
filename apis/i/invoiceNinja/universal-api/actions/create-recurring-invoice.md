# Invoice Ninja: Create Recurring Invoice



```
POST https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-recurring-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-recurring-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "date": "string",
  "dueDate": "string",
  "frequencyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-recurring-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "date": "string",
    "dueDate": "string",
    "frequencyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | The client to bill. |
| `date` | string | yes | The recurring invoice date. |
| `dueDate` | string | yes | The recurring invoice due date. |
| `frequencyId` | string | yes | The recurrence frequency. |
| `remainingCycles` | string | no | Optional number of remaining cycles. |
| `privateNotes` | string | no | Internal recurring invoice notes. |
| `lineItems` | list<object> | no | Line items for the recurring invoice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "archivedAt": 1,
      "autoBill": "string",
      "autoBillEnabled": true,
      "balance": 1,
      "clientId": "string",
      "createdAt": 1,
      "date": "string",
      "documents": [
        {}
      ],
      "dueDate": "string",
      "eInvoice": {},
      "entityType": "string",
      "frequencyId": "string",
      "id": "string",
      "invitations": [
        {}
      ],
      "isDeleted": true,
      "lineItems": [
        {}
      ],
      "nextSendDate": "string",
      "nextSendDatetime": "string",
      "number": "string",
      "paidToDate": 1,
      "privateNotes": "string",
      "publicNotes": "string",
      "recurringDates": [
        {}
      ],
      "remainingCycles": 1,
      "statusId": "string",
      "updatedAt": 1
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
| `autoBill` | string |  |
| `autoBillEnabled` | boolean |  |
| `balance` | number |  |
| `clientId` | string |  |
| `createdAt` | number |  |
| `date` | string |  |
| `documents` | array<object> |  |
| `dueDate` | string |  |
| `eInvoice` | object |  |
| `entityType` | string |  |
| `frequencyId` | string |  |
| `id` | string |  |
| `invitations` | array<object> |  |
| `isDeleted` | boolean |  |
| `lineItems` | array<object> |  |
| `nextSendDate` | string |  |
| `nextSendDatetime` | string |  |
| `number` | string |  |
| `paidToDate` | number |  |
| `privateNotes` | string |  |
| `publicNotes` | string |  |
| `recurringDates` | array<object> |  |
| `remainingCycles` | number |  |
| `statusId` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Invoice Ninja API, this operation is `POST /recurring_invoices` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recurring-invoice.md) for the provider-specific parameters and requirements.

