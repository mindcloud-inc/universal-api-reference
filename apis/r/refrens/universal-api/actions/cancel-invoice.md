# Refrens: Cancel Invoice



```
PUT https://connect.mindcloud.co/v1/universal/refrens/latest/actions/cancel-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refrens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/cancel-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoice": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refrens/latest/actions/cancel-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoice": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoice` | string | yes |  |
| `cancelPayment` | boolean | no | Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "billType": "string",
      "currency": "string",
      "finalTotal": {},
      "invoiceNumber": "string",
      "invoiceTitle": "string",
      "items": [
        {}
      ],
      "payments": [
        {}
      ],
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
| `billType` | string |  |
| `currency` | string |  |
| `finalTotal` | object |  |
| `invoiceNumber` | string |  |
| `invoiceTitle` | string |  |
| `items` | array<object> |  |
| `payments` | array<object> |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Refrens API, this operation is `PATCH /businesses/:urlKey/invoices/:invoice` (base URL `https://api.refrens.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-invoice.md) for the provider-specific parameters and requirements.

