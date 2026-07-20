# Cal.com: Reserve Slot

Creates a slot reservation in Cal.com.

```
POST https://connect.mindcloud.co/v1/universal/cal/latest/actions/reserve-slot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cal/latest/actions/reserve-slot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventTypeId": 1,
  "slotStart": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cal/latest/actions/reserve-slot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventTypeId": 1,
    "slotStart": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventTypeId` | number | yes | Event type ID for the slot reservation. |
| `slotStart` | string | yes | Slot start time in ISO 8601 UTC format. |
| `slotDuration` | number | no | Reserved slot duration in minutes. |
| `reservationDuration` | number | no | Reservation hold duration in minutes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventTypeId": 1,
      "reservationDuration": 1,
      "reservationUid": "string",
      "reservationUntil": "string",
      "slotDuration": 1,
      "slotEnd": "string",
      "slotStart": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventTypeId` | number |  |
| `reservationDuration` | number |  |
| `reservationUid` | string |  |
| `reservationUntil` | string |  |
| `slotDuration` | number |  |
| `slotEnd` | string |  |
| `slotStart` | string |  |

## Native endpoint

Through the native Cal.com API, this operation is `POST /slots/reservations` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reserve-slot.md) for the provider-specific parameters and requirements.

