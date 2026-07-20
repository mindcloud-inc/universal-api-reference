# FleetWire: Update Booking Status

Updates an existing booking status in FleetWire.

```
PUT https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/update-booking-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FleetWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/update-booking-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookingId": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/update-booking-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookingId": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookingId` | string | yes | The FleetWire booking identifier. |
| `status` | string | yes | The new booking status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "booking": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `booking` | object | Updated FleetWire booking payload after the status change. |

## Native endpoint

Through the native FleetWire API, this operation is `PUT /api/v2/bookings/:booking_id/status` (base URL `https://api.fleetwire.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-booking-status.md) for the provider-specific parameters and requirements.

