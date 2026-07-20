# Halo Service Solutions: Create Appointment

Creates a new appointment in Halo Service Solutions.

```
POST https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agent_id": 1,
  "start_date": "2026-05-07T12:00:00.000Z",
  "end_date": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agent_id": 1,
    "start_date": "2026-05-07T12:00:00.000Z",
    "end_date": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticket_id` | number | no |  |
| `agent_id` | number | yes |  |
| `start_date` | date | yes |  |
| `end_date` | date | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent_id": 1,
      "agent_name": "Ava Chen",
      "appointment_type_name": "Ava Chen",
      "client_id": 1,
      "end_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "organizer_email": "ava@example.com",
      "site_id": 1,
      "start_date": "2026-05-07T12:00:00.000Z",
      "subject": "string",
      "ticket_id": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent_id` | number |  |
| `agent_name` | string |  |
| `appointment_type_name` | string |  |
| `client_id` | number |  |
| `end_date` | date |  |
| `id` | number |  |
| `organizer_email` | string |  |
| `site_id` | number |  |
| `start_date` | date |  |
| `subject` | string |  |
| `ticket_id` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `POST /Appointment` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-appointment.md) for the provider-specific parameters and requirements.

