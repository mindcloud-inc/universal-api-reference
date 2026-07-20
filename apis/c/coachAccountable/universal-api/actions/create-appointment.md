# CoachAccountable: Create Appointment

Creates an appointment in CoachAccountable.

```
POST https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1,
  "appointmentTypeId": 1,
  "dateOf": "2026-05-07T12:00:00.000Z",
  "timeOf": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1,
    "appointmentTypeId": 1,
    "dateOf": "2026-05-07T12:00:00.000Z",
    "timeOf": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | yes | The ID of the Client whom the Appointment is with. |
| `appointmentTypeId` | number | yes | The ID of the Appointment Type that the Appointment is to be of |
| `alternateLabel` | string | no | Optional alternate label for the appointment (overrides the Appointment Type's name) |
| `location` | string | no | Optional alternate location for the appointment (overrides the Appointment Type's location) |
| `description` | string | no | Optional alternate description for the appointment (overrides the Appointment Type's description) |
| `dateOf` | date | yes |  |
| `timeOf` | string | yes |  |
| `timezoneOf` | list | no | Who's timezone the appointment date/time is in. Defaults to that of the Coach. One of: `A`, `C`, `L`. |
| `sendNotification` | boolean | no | Send true if the Client should be sent a notification email immediately. Default: `false`. |
| `notificationSubject` | string | no | Subject line of the notification email to be sent (if opted for). If not included, will use template setting. |
| `notificationMessage` | string | no | Body of the notification email to be sent (if opted for). If not included, will use template setting. |
| `reminderSet` | string | no | A semi-colon-separated list of comma-separated triplets, each defining a reminder. In a triplet, the first value defines who to send it to ([C]oach or c[L]ient),the second value defines the send method ([E]mail or [T]ext), and the third value defines when to send the reminder, as minutes relative to the due date. Send "default" to set default reminders defined for the Appointment Type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoachAccountable API returns.

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-appointment.md) for the provider-specific parameters and requirements.

