# Cerbo: Update Appointment

Updates an existing appointment in Cerbo.

```
PUT https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appointment_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-appointment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appointment_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appointment_id` | number | yes | Appointment identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start_date_time` | string | no | Starting datetime of the date range. This field should be formatted as `YYYY-MM-DD HH:MM`. |
| `end_date_time` | string | no | Ending datetime of the date range. This field should be formatted as `YYYY-MM-DD HH:MM`. |
| `provider_ids[]` | array<number> | no | An array of provider identifiers associated with this appointment. |
| `pt_id` | number | no | A patient identifier associated with this appointment. |
| `appointment_type` | string | no | Valid appointment type `name`. |
| `title` | string | no | Display title of the appointment. |
| `appointment_note` | string | no | Accompanying notes for the appointment. |
| `status` | string | no | The status of the appointment. Valid statuses include `scheduled`, `confirmed`, `checked-in`, `in-room`, `cancelled`. Clinic custom statuses may also be used. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `PATCH /appointments/:appointment_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-appointment.md) for the provider-specific parameters and requirements.

