# Halo Service Solutions: Get Appointment

Retrieves an appointment from Halo Service Solutions.

```
GET https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-appointment?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-appointment?${params}`, {
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
| `id` | number | yes | Appointment ID. |

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
      "client_name": "Ava Chen",
      "complete_status": 1,
      "end_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_task": true,
      "site_id": 1,
      "site_name": "Ava Chen",
      "start_date": "2026-05-07T12:00:00.000Z",
      "subject": "string",
      "ticket_id": 1,
      "user_id": 1,
      "user_name": "Ava Chen"
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
| `client_name` | string |  |
| `complete_status` | number |  |
| `end_date` | date |  |
| `id` | number | Appointment ID |
| `is_task` | boolean |  |
| `site_id` | number |  |
| `site_name` | string |  |
| `start_date` | date |  |
| `subject` | string |  |
| `ticket_id` | number |  |
| `user_id` | number |  |
| `user_name` | string |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `GET /Appointment/:id` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-appointment.md) for the provider-specific parameters and requirements.

