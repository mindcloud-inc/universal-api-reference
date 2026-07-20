# Cerbo: List Appointment Reminders

Retrieves appointment reminders from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-appointment-reminders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-appointment-reminders?connectionId=$CONNECTION_ID&appointment_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appointment_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-appointment-reminders?${params}`, {
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
| `appointment_id` | number | yes | ID of the appointment |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `GET /appointments/:appointment_id/reminders` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-appointment-reminders.md) for the provider-specific parameters and requirements.

