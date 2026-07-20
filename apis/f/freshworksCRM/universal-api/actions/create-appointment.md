# Freshworks CRM: Create Appointment

Creates a new appointment in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appointment": {},
  "appointment.endDate": "string",
  "appointment.fromDate": "string",
  "appointment.targetableId": 1,
  "appointment.targetableType": "string",
  "appointment.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appointment": {},
    "appointment.endDate": "string",
    "appointment.fromDate": "string",
    "appointment.targetableId": 1,
    "appointment.targetableType": "string",
    "appointment.title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appointment` | object | yes |  |
| `appointment.description` | string | no |  |
| `appointment.endDate` | string | yes |  |
| `appointment.fromDate` | string | yes |  |
| `appointment.location` | string | no |  |
| `appointment.targetableId` | number | yes |  |
| `appointment.targetableType` | string | yes |  |
| `appointment.timeZone` | string | no |  |
| `appointment.title` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointment": {
        "appointment_attendee_ids": [
          [
            1
          ]
        ],
        "can_checkin": true,
        "can_checkin_checkout": true,
        "checkedin_at": "2026-05-07T12:00:00.000Z",
        "checkedin_duration": 1,
        "checkedout_at": "2026-05-07T12:00:00.000Z",
        "checkedout_latitude": 1,
        "checkedout_location": "string",
        "checkedout_longitude": 1,
        "conference_id": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "creater_id": 1,
        "description": "string",
        "end_date": "2026-05-07T12:00:00.000Z",
        "from_date": "2026-05-07T12:00:00.000Z",
        "has_multiple_emails": true,
        "id": 1,
        "is_allday": true,
        "latitude": 1,
        "location": "string",
        "longitude": 1,
        "note_id": 1,
        "outcome_id": 1,
        "provider": "string",
        "targetables_with_email": [
          [
            {}
          ]
        ],
        "targetables": [
          [
            {}
          ]
        ],
        "time_zone": "string",
        "title": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
      },
      "appointment_attendees": [
        [
          {}
        ]
      ],
      "conferences": [
        [
          {}
        ]
      ],
      "notes": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointment` | object | Created appointment. |
| `appointment_attendees[]` | array<object> | Appointment attendees. |
| `appointment.appointment_attendee_ids[]` | array<number> | Attendee ids. |
| `appointment.can_checkin` | boolean | Checkin availability. |
| `appointment.can_checkin_checkout` | boolean | Checkin/checkout availability. |
| `appointment.checkedin_at` | date | Checked-in timestamp. |
| `appointment.checkedin_duration` | number | Check-in duration. |
| `appointment.checkedout_at` | date | Checked-out timestamp. |
| `appointment.checkedout_latitude` | number | Checked-out latitude. |
| `appointment.checkedout_location` | string | Checked-out location. |
| `appointment.checkedout_longitude` | number | Checked-out longitude. |
| `appointment.conference_id` | number | Conference id. |
| `appointment.created_at` | date | Created timestamp. |
| `appointment.creater_id` | number | Creator id. |
| `appointment.description` | string | Appointment description. |
| `appointment.end_date` | date | End time. |
| `appointment.from_date` | date | Start time. |
| `appointment.has_multiple_emails` | boolean | Multiple email flag. |
| `appointment.id` | number | Appointment identifier. |
| `appointment.is_allday` | boolean | All-day flag. |
| `appointment.latitude` | number | Latitude. |
| `appointment.location` | string | Location. |
| `appointment.longitude` | number | Longitude. |
| `appointment.note_id` | number | Note id. |
| `appointment.outcome_id` | number | Outcome identifier. |
| `appointment.provider` | string | Provider. |
| `appointment.targetables_with_email[]` | array<object> | Linked target records with email. |
| `appointment.targetables_with_email[].id` | number | Target record id. |
| `appointment.targetables_with_email[].name` | string | Target record name. |
| `appointment.targetables_with_email[].type` | string | Target record type. |
| `appointment.targetables[]` | array<object> | Linked target records. |
| `appointment.targetables[].id` | number | Target record id. |
| `appointment.targetables[].type` | string | Target record type. |
| `appointment.time_zone` | string | Time zone. |
| `appointment.title` | string | Appointment title. |
| `appointment.updated_at` | date | Updated timestamp. |
| `conferences[]` | array<object> | Related conferences. |
| `notes[]` | array<object> | Related notes. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/appointments` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-appointment.md) for the provider-specific parameters and requirements.

