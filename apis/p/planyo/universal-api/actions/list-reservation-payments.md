# Planyo: List Reservation Payments

Retrieves reservation payments from Planyo.

```
GET https://connect.mindcloud.co/v1/universal/planyo/latest/actions/list-reservation-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planyo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/list-reservation-payments?connectionId=$CONNECTION_ID&reservationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reservationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planyo/latest/actions/list-reservation-payments?${params}`, {
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
| `reservationId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "couponsUsed": [
        {}
      ],
      "paymentSurcharge": 1,
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `couponsUsed` | array<object> |  |
| `paymentSurcharge` | number |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Planyo API, this operation is `GET /` (base URL `https://www.planyo.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reservation-payments.md) for the provider-specific parameters and requirements.

