# Restoplace: Update Reservation

Updates an existing reservation in Restoplace.

```
PUT https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/update-reservation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restoplace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/update-reservation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restoplace/latest/actions/update-reservation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique Restoplace reservation ID. |
| `from` | string | no | Updated reservation start date and time. |
| `to` | string | no | Updated reservation end date and time. |
| `name` | string | no | Updated guest name. |
| `phone` | string | no | Updated guest phone number. |
| `count` | number | no | Updated number of guests. |
| `itemIds[]` | array<number> | no | Updated booking item IDs. |
| `text` | string | no | Updated reservation comment. |
| `email` | string | no | Updated guest email address. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tgUsername` | string | no | Updated Telegram username without the @ symbol. |
| `source` | string | no | Updated reservation source label. |
| `floorId` | number | no | Updated hall ID. |
| `tags[]` | array<string> | no | Updated reservation tags. |
| `waitlist` | number | no | Whether to move the reservation to the waitlist. |
| `deposit` | number | no | Whether a deposit should be required. |
| `depositTotal` | number | no | Updated total deposit amount. |
| `depositPaid` | number | no | Updated paid deposit amount. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restoplace API returns.

## Native endpoint

Through the native Restoplace API, this operation is `PUT /reserves/:id` (base URL `https://api.restoplace.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reservation.md) for the provider-specific parameters and requirements.

