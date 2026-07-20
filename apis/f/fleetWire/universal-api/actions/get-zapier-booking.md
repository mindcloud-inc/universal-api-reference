# FleetWire: Get Zapier Booking

Retrieves a Zapier booking from FleetWire.

```
GET https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-zapier-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FleetWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-zapier-booking?connectionId=$CONNECTION_ID&bookingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-zapier-booking?${params}`, {
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
| `bookingId` | string | yes | The FleetWire booking identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "booking": {},
      "overlappingBookingIds": [
        "string"
      ],
      "overlappingUnavailableBookingIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `booking` | object | FleetWire Zapier booking payload for the requested booking id. |
| `overlappingBookingIds` | array<string> | Booking IDs that overlap the requested booking when present. |
| `overlappingUnavailableBookingIds` | array<string> | Unavailable overlapping booking IDs when present. |

## Native endpoint

Through the native FleetWire API, this operation is `GET /api/v2/zapier/bookings/:b_id` (base URL `https://api.fleetwire.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-zapier-booking.md) for the provider-specific parameters and requirements.

