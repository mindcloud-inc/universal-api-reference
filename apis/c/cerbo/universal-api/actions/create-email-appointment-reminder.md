# Cerbo: Create Email Appointment Reminder

Creates a new email appointment reminder in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-email-appointment-reminder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-email-appointment-reminder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appointment_id": 1,
  "scheduled_datetime": "string",
  "subject": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-email-appointment-reminder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appointment_id": 1,
    "scheduled_datetime": "string",
    "subject": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appointment_id` | number | yes | ID of the appointment |
| `scheduled_datetime` | string | yes | Datetime for the reminder to be sent. This field should be formatted as `YYYY-MM-DD HH:MM`. |
| `subject` | string | yes | Subject for the reminder email. |
| `text` | string | yes | Body of the reminder email. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `POST /appointments/:appointment_id/reminders/email` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-appointment-reminder.md) for the provider-specific parameters and requirements.

