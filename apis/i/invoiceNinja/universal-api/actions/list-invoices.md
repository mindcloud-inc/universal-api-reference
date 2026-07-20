# Invoice Ninja: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-invoices?${params}`, {
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
| `clientId` | string | no | Filter invoices by client id. |
| `filter` | string | no | Text filter for invoice search. |
| `status` | string | no | Filter invoices by status values such as active, archived, or deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "archivedAt": 1,
      "autoBillEnabled": true,
      "backup": {},
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
      "id": "string",
      "invitations": [
        {}
      ],
      "isDeleted": true,
      "lineItems": [
        {}
      ],
      "number": "string",
      "paidToDate": 1,
      "privateNotes": "string",
      "publicNotes": "string",
      "statusId": "string",
      "taxInfo": {},
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
| `autoBillEnabled` | boolean |  |
| `backup` | object |  |
| `balance` | number |  |
| `clientId` | string |  |
| `createdAt` | number |  |
| `date` | string |  |
| `documents` | array<object> |  |
| `dueDate` | string |  |
| `eInvoice` | object |  |
| `entityType` | string |  |
| `id` | string |  |
| `invitations` | array<object> |  |
| `isDeleted` | boolean |  |
| `lineItems` | array<object> |  |
| `number` | string |  |
| `paidToDate` | number |  |
| `privateNotes` | string |  |
| `publicNotes` | string |  |
| `statusId` | string |  |
| `taxInfo` | object |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Invoice Ninja API, this operation is `GET /invoices` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

