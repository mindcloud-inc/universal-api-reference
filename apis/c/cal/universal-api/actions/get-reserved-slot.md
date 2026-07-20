# Cal.com: Get Reserved Slot

Retrieves a reserved slot from Cal.com.

```
GET https://connect.mindcloud.co/v1/universal/cal/latest/actions/get-reserved-slot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cal/latest/actions/get-reserved-slot?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cal/latest/actions/get-reserved-slot?${params}`, {
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
| `uid` | string | yes | Reservation UID from Cal.com path parameter. |

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

Through the native Cal.com API, this operation is `GET /slots/reservations/:uid` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reserved-slot.md) for the provider-specific parameters and requirements.

