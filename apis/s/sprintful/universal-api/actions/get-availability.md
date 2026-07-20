# Sprintful: Get Availability

Retrieves booking page availability from Sprintful.

```
GET https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/get-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sprintful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/get-availability?connectionId=$CONNECTION_ID&slug=sample-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "sample-page"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/get-availability?${params}`, {
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
| `slug` | string | yes | The Sprintful booking page slug. Default: `sample-page`. |
| `startDate` | string | no | Availability window start date. Sprintful format: DD-MM-YYY. Default: `27-03-2026`. |
| `endDate` | string | no | Availability window end date. Sprintful format: DD-MM-YYY. Default: `03-04-2026`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "appointments": {
          "capacity": 1,
          "duration": 1,
          "name": "Ava Chen",
          "slots": {
            "available": true,
            "availableSeatsCount": 1,
            "from": "string",
            "to": "string",
            "unavailableReason": "string"
          }
        },
        "timezone": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Sprintful availability for the requested page. |
| `data.appointments` | array<object> | Appointment types and their available slots. |
| `data.appointments.capacity` | number | Appointment capacity. |
| `data.appointments.duration` | number | Appointment duration in minutes. |
| `data.appointments.name` | string | Appointment name. |
| `data.appointments.slots` | array<object> | Availability slots for the appointment. |
| `data.appointments.slots.available` | boolean | Whether the slot can be booked. |
| `data.appointments.slots.availableSeatsCount` | number | Remaining seat count for the slot. |
| `data.appointments.slots.from` | string | Slot start timestamp. |
| `data.appointments.slots.to` | string | Slot end timestamp. |
| `data.appointments.slots.unavailableReason` | string | Reason the slot is unavailable when Sprintful provides one. |
| `data.timezone` | string | Timezone used for availability calculations. |
| `success` | boolean | Whether the Sprintful request succeeded. |

## Native endpoint

Through the native Sprintful API, this operation is `GET /availability/:slug` (base URL `https://app.sprintful.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-availability.md) for the provider-specific parameters and requirements.

