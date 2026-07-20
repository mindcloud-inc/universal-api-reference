# Syncro: Update Invoice

Updates an existing invoice in Syncro.

```
PUT https://connect.mindcloud.co/v1/universal/syncro/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncro/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Required invoice ID to update. |
| `customerId` | number | no |  |
| `number` | string | no |  |
| `date` | date | no |  |
| `customerBusinessThenName` | string | no |  |
| `createdAt` | date | no |  |
| `updatedAt` | date | no |  |
| `dueDate` | date | no |  |
| `subtotal` | string | no |  |
| `total` | string | no |  |
| `tax` | string | no |  |
| `ticketId` | number | no |  |
| `pdfUrl` | string | no |  |
| `locationId` | number | no |  |
| `poNumber` | string | no |  |
| `contactId` | number | no |  |
| `note` | string | no |  |
| `hardwarecost` | number | no |  |

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

Through the native Syncro API, this operation is `PUT /invoices/:id` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

