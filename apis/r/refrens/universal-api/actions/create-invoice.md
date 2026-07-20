# Refrens: Create Invoice



```
POST https://connect.mindcloud.co/v1/universal/refrens/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refrens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "billedTo": {},
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refrens/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "billedTo": {},
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billedTo` | object | yes | Customer billing object for the invoice. |
| `items[]` | array<object> | yes | Invoice line items array. |
| `invoiceNumber` | string | no | Optional invoice number. |
| `invoiceDate` | date | no | Invoice date. |
| `currency` | string | no | Invoice currency code. Default: `INR`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "billedBy": {},
      "billedTo": {},
      "billType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "finalTotal": {},
      "invoiceDate": "2026-05-07T12:00:00.000Z",
      "invoiceNumber": "string",
      "items": [
        {}
      ],
      "share": {},
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `billedBy` | object |  |
| `billedTo` | object |  |
| `billType` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `finalTotal` | object |  |
| `invoiceDate` | date |  |
| `invoiceNumber` | string |  |
| `items` | array<object> |  |
| `share` | object |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Refrens API, this operation is `POST /businesses/:urlKey/invoices` (base URL `https://api.refrens.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

