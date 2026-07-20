# Freshworks CRM: Get Appointment

Retrieves a appointment from Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-appointment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-appointment?${params}`, {
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
| `id` | string | yes |  |

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
        "targetable": {
          "id": 1,
          "type": "string"
        },
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
      "contacts": [
        [
          {}
        ]
      ],
      "notes": [
        [
          {}
        ]
      ],
      "users": [
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
| `appointment` | object | Appointment record. |
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
| `appointment.targetable.id` | number | Linked target id. |
| `appointment.targetable.type` | string | Linked target type. |
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
| `contacts[]` | array<object> | Related contacts. |
| `contacts[].avatar` | string | Avatar URL. |
| `contacts[].display_name` | string | Display name. |
| `contacts[].email` | string | Email address. |
| `contacts[].first_name` | string | First name. |
| `contacts[].id` | number | Contact identifier. |
| `contacts[].job_title` | string | Job title. |
| `contacts[].last_name` | string | Last name. |
| `contacts[].linkedin` | string | LinkedIn profile. |
| `contacts[].mobile_number` | string | Mobile number. |
| `contacts[].subscription_status` | number | Subscription status. |
| `contacts[].subscription_types` | string | Subscription types. |
| `contacts[].work_number` | string | Work number. |
| `notes[]` | array<object> | Related notes. |
| `users[]` | array<object> | Related users. |
| `users[].display_name` | string | Display name. |
| `users[].email` | string | Email address. |
| `users[].id` | number | User identifier. |
| `users[].is_active` | boolean | Active flag. |
| `users[].mobile_number` | string | Mobile number. |
| `users[].work_number` | string | Work number. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET /api/appointments/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-appointment.md) for the provider-specific parameters and requirements.

