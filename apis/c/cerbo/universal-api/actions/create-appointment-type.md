# Cerbo: Create Appointment Type

Creates a new appointment type in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-appointment-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-appointment-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "default_length": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-appointment-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "default_length": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the appointment type. Must be unique and contain at least one letter or number. |
| `default_length` | number | yes | Default duration in minutes. Must be between 5 minutes and 12 hours (720 minutes). |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name_portal` | string | no | Name displayed on the patient portal. Defaults to the same value as name if not specified. |
| `color_hex` | string | no | Six-character hexadecimal color code (without #) for calendar display. A random color is assigned if not specified. |
| `description` | string | no | Internal description of the appointment type. |
| `allow_on_portal` | boolean | no | Whether patients can book this type via the portal. Default: `false`. |
| `number_of_overlaps_to_allow` | number | no | Maximum concurrent appointments of this type allowed (for group appointments). Default: `1`. |
| `portal_notice` | string | no | Notice displayed to patients when booking via portal. |
| `which_providers[]` | array<number> | no | Array of provider IDs who can have this appointment type. Use [0] for all providers. |
| `sort_order` | number | no | Display order in appointment type lists. Default: `0`. |
| `telemedicine` | boolean | no | Whether this is a telemedicine appointment type. Default: `false`. |
| `email_notice_on` | boolean | no | Send email notification when appointment is created. Default: `false`. |
| `email_notice` | string | no | Email body for appointment creation notification. |
| `email_notice_subject` | string | no | Subject line for appointment creation email. Default: `You have a new appointment`. |
| `email_reminder_on` | boolean | no | Send automated email reminder before appointment. Default: `false`. |
| `email_reminder` | string | no | Email body for reminder. |
| `email_reminder_subject` | string | no | Subject line for reminder email. Default: `Reminder about your upcoming appointment`. |
| `email_reminder_hrs_before` | number | no | Hours before appointment to send email reminder (1 hour to 30 days). Default: `48`. |
| `sms_reminder_on` | boolean | no | Send automated SMS reminder before appointment. Default: `false`. |
| `sms_reminder` | string | no | SMS message text for reminder (max 220 characters). |
| `sms_reminder_hrs_before` | number | no | Hours before appointment to send SMS reminder (1 hour to 30 days). Default: `24`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_on_portal": true,
      "color_hex": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "created_by": 1,
      "default_length": 1,
      "description": "string",
      "email_notice": "ava@example.com",
      "email_notice_on": true,
      "email_notice_subject": "ava@example.com",
      "email_reminder": "ava@example.com",
      "email_reminder_hrs_before": 1,
      "email_reminder_on": true,
      "email_reminder_subject": "ava@example.com",
      "id": 1,
      "inactive_date": "string",
      "is_active": true,
      "name": "Ava Chen",
      "name_portal": "Ava Chen",
      "number_of_overlaps_to_allow": 1,
      "object": "string",
      "portal_notice": "string",
      "sms_reminder": "string",
      "sms_reminder_hrs_before": 1,
      "sms_reminder_on": true,
      "sort_order": 1,
      "telemedicine": true,
      "which_providers": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_on_portal` | boolean |  |
| `color_hex` | string |  |
| `created` | date |  |
| `created_by` | number |  |
| `default_length` | number |  |
| `description` | string |  |
| `email_notice` | string |  |
| `email_notice_on` | boolean |  |
| `email_notice_subject` | string |  |
| `email_reminder` | string |  |
| `email_reminder_hrs_before` | number |  |
| `email_reminder_on` | boolean |  |
| `email_reminder_subject` | string |  |
| `id` | number |  |
| `inactive_date` | string |  |
| `is_active` | boolean |  |
| `name` | string |  |
| `name_portal` | string |  |
| `number_of_overlaps_to_allow` | number |  |
| `object` | string |  |
| `portal_notice` | string |  |
| `sms_reminder` | string |  |
| `sms_reminder_hrs_before` | number |  |
| `sms_reminder_on` | boolean |  |
| `sort_order` | number |  |
| `telemedicine` | boolean |  |
| `which_providers` | array<number> |  |

## Native endpoint

Through the native Cerbo API, this operation is `POST /appointment_types` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-appointment-type.md) for the provider-specific parameters and requirements.

