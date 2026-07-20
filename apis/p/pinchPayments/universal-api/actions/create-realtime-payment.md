# Pinch Payments: Create Realtime Payment

Creates a realtime payment in Pinch Payments.

```
POST https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-realtime-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinch Payments `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-realtime-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-realtime-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1
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
| `email` | string | no |  |
| `firstName` | string | no |  |
| `fullName` | string | no |  |
| `lastName` | string | no |  |
| `metadata` | string | no |  |
| `mobileNumber` | string | no |  |
| `nonce[]` | array | no |  |
| `payerId` | string | no |  |
| `sourceId` | string | no |  |
| `surcharge[]` | array | no |  |
| `token` | string | no |  |

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

Through the native Pinch Payments API, this operation is `POST /payments/realtime` (base URL `https://api.getpinch.com.au/live`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-realtime-payment.md) for the provider-specific parameters and requirements.

