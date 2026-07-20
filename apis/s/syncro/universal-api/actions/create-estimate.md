# Syncro: Create Estimate

Creates a new estimate in Syncro.

```
POST https://connect.mindcloud.co/v1/universal/syncro/latest/actions/create-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/create-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "date": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncro/latest/actions/create-estimate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "date": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | Required customer record ID for the estimate. |
| `date` | date | yes | Required estimate date. |
| `number` | string | no |  |
| `name` | string | no |  |
| `status` | string | no | Valid values are Fresh, Draft, Approved, Declined. |
| `ticketId` | number | no |  |
| `locationId` | number | no |  |
| `note` | string | no |  |
| `lineItems[]` | array<object> | no | Array of estimate line item objects. |
| `lineItems[].item` | string | no |  |
| `lineItems[].name` | string | no |  |
| `lineItems[].productId` | number | no |  |
| `lineItems[].quantity` | number | no |  |
| `createdAt` | date | no |  |
| `updatedAt` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerBusinessThenName": "Ava Chen",
      "customerId": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "employee": "string",
      "id": 1,
      "invoiceId": 1,
      "locationId": 1,
      "name": "Ava Chen",
      "number": "string",
      "pdfUrl": "https://example.com",
      "status": "string",
      "subtotal": "string",
      "tax": "string",
      "ticketId": 1,
      "total": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `customerBusinessThenName` | string |  |
| `customerId` | number |  |
| `date` | date |  |
| `employee` | string |  |
| `id` | number |  |
| `invoiceId` | number |  |
| `locationId` | number |  |
| `name` | string |  |
| `number` | string |  |
| `pdfUrl` | string |  |
| `status` | string |  |
| `subtotal` | string |  |
| `tax` | string |  |
| `ticketId` | number |  |
| `total` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Syncro API, this operation is `POST /estimates` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-estimate.md) for the provider-specific parameters and requirements.

