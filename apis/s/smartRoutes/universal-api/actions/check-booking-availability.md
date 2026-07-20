# SmartRoutes: Check Booking Availability



```
GET https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/check-booking-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartRoutes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/check-booking-availability?connectionId=$CONNECTION_ID&date=string&order.type=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string",
  "order.type": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/check-booking-availability?${params}`, {
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
| `date` | string | yes | Requested date for booking availability in YYYY-MM-DD format. |
| `order.type` | string | yes | Whether to check delivery or pickup availability. One of: `0`, `1`. |
| `order.deliveryLat` | number | no | Delivery latitude for availability checks. |
| `order.deliveryLng` | number | no | Delivery longitude for availability checks. |
| `order.deliveryDuration` | number | no | Delivery duration in minutes. |
| `order.pickupLat` | number | no | Pickup latitude for availability checks. |
| `order.pickupLng` | number | no | Pickup longitude for availability checks. |
| `order.pickupDuration` | number | no | Pickup duration in minutes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | boolean | Whether the booking request is currently available. |

## Native endpoint

Through the native SmartRoutes API, this operation is `POST /booking/availability` (base URL `https://api.smartroutes.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-booking-availability.md) for the provider-specific parameters and requirements.

