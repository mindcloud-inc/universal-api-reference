# Refrens: Add Invoice Payment



```
POST https://connect.mindcloud.co/v1/universal/refrens/latest/actions/add-invoice-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refrens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/add-invoice-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoice": "string",
  "amount": 1,
  "paymentDate": "2026-05-07T12:00:00.000Z",
  "paymentMethod": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refrens/latest/actions/add-invoice-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoice": "string",
    "amount": 1,
    "paymentDate": "2026-05-07T12:00:00.000Z",
    "paymentMethod": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoice` | string | yes |  |
| `amount` | number | yes |  |
| `paymentDate` | date | yes |  |
| `paymentMethod` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "amount": 1,
      "appId": "string",
      "business": "string",
      "isApproved": true,
      "isRemoved": true,
      "notes": "string",
      "payerBusiness": "string",
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "paymentMethod": "string",
      "tds": 1,
      "transactionCharge": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `amount` | number |  |
| `appId` | string |  |
| `business` | string |  |
| `isApproved` | boolean |  |
| `isRemoved` | boolean |  |
| `notes` | string |  |
| `payerBusiness` | string |  |
| `paymentDate` | date |  |
| `paymentMethod` | string |  |
| `tds` | number |  |
| `transactionCharge` | number |  |

## Native endpoint

Through the native Refrens API, this operation is `POST /businesses/:urlKey/invoices/:invoice/payments` (base URL `https://api.refrens.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-invoice-payment.md) for the provider-specific parameters and requirements.

