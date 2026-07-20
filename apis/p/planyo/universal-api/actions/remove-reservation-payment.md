# Planyo: Remove Reservation Payment

Deletes a reservation payment from Planyo.

```
DELETE https://connect.mindcloud.co/v1/universal/planyo/latest/actions/remove-reservation-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/remove-reservation-payment?connectionId=$CONNECTION_ID&paymentId=1&reservationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentId": "1",
  "reservationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planyo/latest/actions/remove-reservation-payment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paymentId` | number | yes |  |
| `reservationId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paymentId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paymentId` | number |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-reservation-payment.md) for the provider-specific parameters and requirements.

