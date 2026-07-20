# Invoice Ninja: List Recurring Invoices



```
GET https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-recurring-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-recurring-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-recurring-invoices?${params}`, {
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
| `clientId` | string | no | Filter by client. |
| `frequencyId` | string | no | Filter by recurrence frequency. |
| `filter` | string | no | Free-text filter value. |

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

Through the native Invoice Ninja API, this operation is `GET /recurring_invoices` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-recurring-invoices.md) for the provider-specific parameters and requirements.

