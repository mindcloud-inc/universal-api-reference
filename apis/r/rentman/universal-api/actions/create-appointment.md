# Rentman: Create Appointment



```
POST https://connect.mindcloud.co/v1/universal/rentman/latest/actions/create-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rentman/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "start": "2026-05-07T12:00:00.000Z",
    "end": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Appointment name. |
| `start` | date | yes | Appointment start timestamp. |
| `end` | date | yes | Appointment end timestamp. |
| `location` | string | no | Appointment location. |
| `remark` | string | no | Appointment remark. |
| `is_public` | boolean | no | Whether the appointment is public. |
| `is_plannable` | boolean | no | Whether employees can be scheduled during this appointment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "displayname": "Ava Chen",
      "end": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_plannable": true,
      "is_public": true,
      "location": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "recurrence_enddate": "2026-05-07T12:00:00.000Z",
      "recurrence_group": 1,
      "recurrence_interval": 1,
      "recurrence_interval_unit": "string",
      "recurrence_weekdays": "string",
      "remark": "string",
      "start": "2026-05-07T12:00:00.000Z",
      "synchronisation_uri": "string",
      "synchronization_id": "string",
      "updateHash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `created` | date |  |
| `creator` | string |  |
| `displayname` | string |  |
| `end` | date |  |
| `id` | number |  |
| `is_plannable` | boolean |  |
| `is_public` | boolean |  |
| `location` | string |  |
| `modified` | date |  |
| `name` | string |  |
| `recurrence_enddate` | date |  |
| `recurrence_group` | number |  |
| `recurrence_interval` | number |  |
| `recurrence_interval_unit` | string |  |
| `recurrence_weekdays` | string |  |
| `remark` | string |  |
| `start` | date |  |
| `synchronisation_uri` | string |  |
| `synchronization_id` | string |  |
| `updateHash` | string |  |

## Native endpoint

Through the native Rentman API, this operation is `POST /appointments` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-appointment.md) for the provider-specific parameters and requirements.

