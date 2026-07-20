# Flexopus: Create Booking

Creates a new booking in Flexopus.

```
POST https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/create-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookableId": 1,
  "toTime": "2026-05-07T12:00:00.000Z",
  "userId": 1,
  "locationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookableId": 1,
    "toTime": "2026-05-07T12:00:00.000Z",
    "userId": 1,
    "locationId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookableId` | number | yes | ID of the bookable to reserve. |
| `fromTime` | date | no | When the booking will start. |
| `toTime` | date | yes | When the booking will end. |
| `userId` | number | yes | ID of the user for whom the reservation is made. |
| `locationId` | number | yes | ID of the location for the reservation. |
| `guestEmail` | string | no | Guest email address for a guest booking. |
| `guestName` | string | no | Guest name for a guest booking. |
| `bookingInfo` | string | no | Purpose of the booking for a guest booking. |
| `userVehicleId` | number | no | Vehicle ID when reserving a parking space. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "bookable": {
            "id": 1,
            "name": "Ava Chen",
            "status": 1,
            "type": 1
          },
          "from": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "livemap": "string",
          "to": "2026-05-07T12:00:00.000Z",
          "user": {
            "email": "ava@example.com",
            "extensionAttributes": {},
            "id": 1,
            "name": "Ava Chen"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].bookable` | object |  |
| `data[].bookable.id` | number |  |
| `data[].bookable.name` | string |  |
| `data[].bookable.status` | number |  |
| `data[].bookable.type` | number |  |
| `data[].from` | date |  |
| `data[].id` | number |  |
| `data[].livemap` | string |  |
| `data[].to` | date |  |
| `data[].user` | object |  |
| `data[].user.email` | string |  |
| `data[].user.extensionAttributes` | object |  |
| `data[].user.id` | number |  |
| `data[].user.name` | string |  |

## Native endpoint

Through the native Flexopus API, this operation is `POST /bookings` (base URL `{{credentials.tenantBaseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking.md) for the provider-specific parameters and requirements.

