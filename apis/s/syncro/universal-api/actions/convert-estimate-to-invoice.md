# Syncro: Convert Estimate To Invoice

Creates an invoice from an estimate in Syncro.

```
POST https://connect.mindcloud.co/v1/universal/syncro/latest/actions/convert-estimate-to-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/convert-estimate-to-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncro/latest/actions/convert-estimate-to-invoice', {
  method: 'POST',
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
| `id` | number | yes |  |

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
      "externalId": "string",
      "hardwarecost": "string",
      "id": 1,
      "isPaid": true,
      "locationId": 1,
      "name": "Ava Chen",
      "note": "string",
      "number": "string",
      "pdfUrl": "https://example.com",
      "poNumber": "string",
      "qbsdkExternalId": "string",
      "scheduleId": 1,
      "subtotal": "string",
      "tax": "string",
      "techMarkedPaid": true,
      "ticketId": 1,
      "total": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "verifiedPaid": true,
      "xeroId": "string"
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
| `externalId` | string |  |
| `hardwarecost` | string |  |
| `id` | number |  |
| `isPaid` | boolean |  |
| `locationId` | number |  |
| `name` | string |  |
| `note` | string |  |
| `number` | string |  |
| `pdfUrl` | string |  |
| `poNumber` | string |  |
| `qbsdkExternalId` | string |  |
| `scheduleId` | number |  |
| `subtotal` | string |  |
| `tax` | string |  |
| `techMarkedPaid` | boolean |  |
| `ticketId` | number |  |
| `total` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |
| `verifiedPaid` | boolean |  |
| `xeroId` | string |  |

## Native endpoint

Through the native Syncro API, this operation is `POST /estimates/:id/convert_to_invoice` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-estimate-to-invoice.md) for the provider-specific parameters and requirements.

