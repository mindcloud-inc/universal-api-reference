# Syncro: Create Invoice

Creates a new invoice in Syncro.

```
POST https://connect.mindcloud.co/v1/universal/syncro/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "number": "string",
  "date": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncro/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "number": "string",
    "date": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | Required customer record ID for the new invoice. |
| `number` | string | yes | Required invoice number string. |
| `date` | date | yes | Required invoice date. |
| `dueDate` | date | no |  |
| `ticketId` | number | no |  |
| `locationId` | number | no |  |
| `contactId` | number | no |  |
| `poNumber` | string | no |  |
| `note` | string | no |  |
| `lineItems[]` | array<object> | no | Array of invoice line item objects. |
| `lineItems[].item` | string | no |  |
| `lineItems[].name` | string | no |  |
| `lineItems[].productId` | number | no |  |
| `lineItems[].quantity` | number | no |  |
| `lineItems[].cost` | number | no |  |
| `lineItems[].price` | number | no |  |
| `lineItems[].discountPercent` | number | no |  |
| `lineItems[].taxable` | boolean | no |  |
| `lineItems[].upcCode` | string | no |  |
| `lineItems[].taxNote` | string | no |  |
| `lineItems[].wholesale` | number | no |  |
| `lineItems[].invoiceBundleId` | number | no |  |
| `lineItems[].taxRateId` | number | no |  |
| `lineItems[].userId` | number | no |  |
| `lineItems[].position` | number | no |  |
| `id` | number | no | Explicit invoice ID field documented in Syncro's create payload schema. |
| `balanceDue` | number | no |  |
| `customerBusinessThenName` | string | no |  |
| `createdAt` | date | no |  |
| `updatedAt` | date | no |  |
| `subtotal` | string | no |  |
| `total` | string | no |  |
| `tax` | string | no |  |
| `verifiedPaid` | boolean | no |  |
| `techMarkedPaid` | boolean | no |  |
| `pdfUrl` | string | no |  |
| `isPaid` | boolean | no |  |
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

Through the native Syncro API, this operation is `POST /invoices` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

