# Syncro: List Invoices

Retrieves a list of invoices from Syncro.

```
GET https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-invoices?${params}`, {
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
| `paid` | boolean | no | Return invoices marked as paid. |
| `unpaid` | boolean | no | Return invoices marked as unpaid. |
| `ticketId` | number | no | Return invoices attached to a specific ticket ID. |
| `sinceUpdatedAt` | date | no | Return invoices updated since the provided date. |
| `page` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerBusinessThenName": "Ava Chen",
      "customerId": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "hardwarecost": "string",
      "id": 1,
      "isPaid": true,
      "locationId": 1,
      "note": "string",
      "number": "string",
      "pdfUrl": "https://example.com",
      "poNumber": "string",
      "subtotal": "string",
      "tax": "string",
      "techMarkedPaid": true,
      "ticketId": 1,
      "total": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "verifiedPaid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |
| `createdAt` | date |  |
| `customerBusinessThenName` | string |  |
| `customerId` | number |  |
| `date` | date |  |
| `dueDate` | date |  |
| `hardwarecost` | string |  |
| `id` | number |  |
| `isPaid` | boolean |  |
| `locationId` | number |  |
| `note` | string |  |
| `number` | string |  |
| `pdfUrl` | string |  |
| `poNumber` | string |  |
| `subtotal` | string |  |
| `tax` | string |  |
| `techMarkedPaid` | boolean |  |
| `ticketId` | number |  |
| `total` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `verifiedPaid` | boolean |  |

## Native endpoint

Through the native Syncro API, this operation is `GET /invoices` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

