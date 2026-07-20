# Planyo: Add Reservation Payment

Adds a reservation payment in Planyo.

```
POST https://connect.mindcloud.co/v1/universal/planyo/latest/actions/add-reservation-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/add-reservation-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reservationId": 1,
  "paymentMode": 1,
  "paymentStatus": 1,
  "transactionId": "string",
  "amount": 1,
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planyo/latest/actions/add-reservation-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reservationId": 1,
    "paymentMode": 1,
    "paymentStatus": 1,
    "transactionId": "string",
    "amount": 1,
    "currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reservationId` | number | yes |  |
| `paymentMode` | number | yes |  |
| `paymentStatus` | number | yes |  |
| `transactionId` | string | yes |  |
| `amount` | number | yes |  |
| `currency` | string | yes |  |
| `paymentTime` | string | no |  |
| `extraInfo` | string | no |  |
| `isQuiet` | boolean | no |  |
| `paymentResponseCode` | string | no |  |
| `transactionStatusText` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paymentId": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paymentId` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-reservation-payment.md) for the provider-specific parameters and requirements.

