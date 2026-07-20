# Restoplace: Create Reservation

Creates a new reservation in Restoplace.

```
POST https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/create-reservation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restoplace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/create-reservation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/create-reservation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | no | Reservation start date and time in the provider-supported format. |
| `to` | string | no | Reservation end date and time in the provider-supported format. |
| `name` | string | no | Guest name for the reservation. |
| `phone` | string | no | Guest phone number. |
| `count` | number | no | Number of guests for the reservation. |
| `itemIds[]` | array<number> | no | Booking item IDs to reserve. |
| `text` | string | no | Optional reservation comment. |
| `email` | string | no | Guest email address. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tgUsername` | string | no | Telegram username without the @ symbol. |
| `source` | string | no | Reservation source label such as widget, admin, or api. |
| `floorId` | number | no | Hall ID to use when the reservation is tied to a hall instead of specific booking items. |
| `tags[]` | array<string> | no | Reservation tags to attach to the booking. |
| `waitlist` | number | no | Whether the reservation should be added to the waitlist. |
| `deposit` | number | no | Whether a deposit should be required for this reservation. |
| `depositTotal` | number | no | Total deposit amount expected for the reservation. |
| `depositPaid` | number | no | Deposit amount already paid for the reservation. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restoplace API returns.

## Native endpoint

Through the native Restoplace API, this operation is `POST /reserves/` (base URL `https://api.restoplace.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reservation.md) for the provider-specific parameters and requirements.

