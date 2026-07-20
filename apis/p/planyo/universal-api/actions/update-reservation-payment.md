# Planyo: Update Reservation Payment

Updates a reservation payment in Planyo.

```
PUT https://connect.mindcloud.co/v1/universal/planyo/latest/actions/update-reservation-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/update-reservation-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paymentId": 1,
  "reservationId": 1,
  "paymentStatus": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planyo/latest/actions/update-reservation-payment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paymentId": 1,
    "reservationId": 1,
    "paymentStatus": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paymentId` | number | yes |  |
| `reservationId` | number | yes |  |
| `paymentStatus` | number | yes |  |
| `extraInfo` | string | no |  |

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

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reservation-payment.md) for the provider-specific parameters and requirements.

