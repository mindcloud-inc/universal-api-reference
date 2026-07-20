# Cerbo: Create Appointment

Creates a new appointment in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "start_date_time": "string",
  "end_date_time": "string",
  "provider_ids[]": [
    1
  ],
  "appointment_type": "string",
  "title": "string",
  "appointment_note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "start_date_time": "string",
    "end_date_time": "string",
    "provider_ids[]": [1],
    "appointment_type": "string",
    "title": "string",
    "appointment_note": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start_date_time` | string | yes | Starting datetime of the date range. This field should be formatted as `YYYY-MM-DD HH:MM`. |
| `end_date_time` | string | yes | Ending datetime of the date range. This field should be formatted as `YYYY-MM-DD HH:MM`. |
| `provider_ids[]` | array<number> | yes | An array of provider identifiers associated with this appointment. |
| `appointment_type` | string | yes | Valid appointment type `name`. |
| `title` | string | yes | Display title of the appointment. |
| `appointment_note` | string | yes | Accompanying notes for the appointment. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pt_id` | number | no | A patient identifier associated with this appointment. |
| `status` | string | no | The status of the appointment. Valid statuses include `scheduled`, `confirmed`, `checked-in`, `in-room`, `cancelled`. Clinic custom statuses may also be used. Default: `scheduled`. |
| `telemedicine` | boolean | no | Flag for whether or not this is a telemedicine appointment. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `POST /appointments` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-appointment.md) for the provider-specific parameters and requirements.

