# Quilia: Create Appointment



```
POST https://connect.mindcloud.co/v1/universal/quilia/latest/actions/create-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quilia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quilia/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "caseId": "string",
  "start": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quilia/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "caseId": "string",
    "start": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `caseId` | string | yes | The case ID to associate with the appointment. Links the appointment to a specific legal case or matter. |
| `contactId` | string | no | The contact/people ID associated with the appointment. Identifies the person involved in the appointment. Optional for legal appointments. |
| `notes` | string | no | Additional notes or details about the appointment. Can include agenda items, special instructions, or other relevant information. |
| `title` | string | no | Title/name of the appointment. Recommended for legal appointments. |
| `userId` | string | no | The user ID to assign the appointment to. If provided, this user will be responsible for the appointment. |
| `start` | date | yes | ISO 8601 timestamp for when the appointment starts. Must be a valid datetime string. |
| `end` | date | no | ISO 8601 timestamp for when the appointment ends. Required for legal appointments. |
| `type` | list<string> | no | Type of appointment: 'medical' for medical appointments, 'legal' for legal calendar events. One of: `legal`, `medical`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Quilia API returns.

## Native endpoint

Through the native Quilia API, this operation is `POST appointments` (base URL `https://api.quilia.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-appointment.md) for the provider-specific parameters and requirements.

