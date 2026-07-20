# Pinch Payments: Create or Update Payment

Creates or updates a scheduled payment in Pinch Payments.

```
POST https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-or-update-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinch Payments `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-or-update-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "payerId": "string",
  "transactionDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-or-update-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "payerId": "string",
    "transactionDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes |  |
| `applicationFee` | number | no |  |
| `description` | string | no |  |
| `id` | string | no |  |
| `nonce[]` | array | no |  |
| `payerId` | string | yes |  |
| `sourceId` | string | no |  |
| `surcharge[]` | array | no |  |
| `transactionDate` | date | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Pinch Payments API, this operation is `POST /payments` (base URL `https://api.getpinch.com.au/live`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-payment.md) for the provider-specific parameters and requirements.

