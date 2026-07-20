# Timewax: Create Planning Booking

Creates a new planning booking in Timewax.

```
POST https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-planning-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-planning-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request.entry.type": "string",
  "request.entry.project": "string",
  "request.entry.breakdown": "string",
  "request.entry.date": "2026-05-07T12:00:00.000Z",
  "request.entry.timeFrom": "string",
  "request.entry.hours": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timewax/latest/actions/create-planning-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request.entry.type": "string",
    "request.entry.project": "string",
    "request.entry.breakdown": "string",
    "request.entry.date": "2026-05-07T12:00:00.000Z",
    "request.entry.timeFrom": "string",
    "request.entry.hours": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request.entry.type` | string | yes | Required. Booking type: entry for bookings with resources, request for bookings without resources. |
| `request.entry.resource` | string | no | Resource code or name for entry bookings. |
| `request.entry.project` | string | yes | Required. Code or name of the project. |
| `request.entry.breakdown` | string | yes | Required. Code or name of the activity. |
| `request.entry.date` | date | yes | Required. Date of the booking, format yyyymmdd or yyyy-mm-dd. |
| `request.entry.timeFrom` | string | yes | Required. Start time for the booking, format hh:mm. |
| `request.entry.hours` | number | yes | Required. Number of hours. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "valid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `valid` | string | Operation validity indicator. |

## Native endpoint

Through the native Timewax API, this operation is `POST calendar/entries/add/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-planning-booking.md) for the provider-specific parameters and requirements.

