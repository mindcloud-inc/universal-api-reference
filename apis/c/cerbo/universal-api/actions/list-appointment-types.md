# Cerbo: List Appointment Types

Retrieves appointment types from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-appointment-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-appointment-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-appointment-types?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include_deleted` | string | no | If specified and not empty, results will include deleted appointment types. Any non-empty value is treated as true. |

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
      "default_status": "string",
      "description": "string",
      "email_notice": "ava@example.com",
      "email_notice_on": true,
      "email_notice_subject": "ava@example.com",
      "email_reminder_hrs_before": 1,
      "email_reminder_on": true,
      "id": 1,
      "inactive_date": "2026-05-07T12:00:00.000Z",
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
| `default_status` | string |  |
| `description` | string |  |
| `email_notice` | string |  |
| `email_notice_on` | boolean |  |
| `email_notice_subject` | string |  |
| `email_reminder_hrs_before` | number |  |
| `email_reminder_on` | boolean |  |
| `id` | number |  |
| `inactive_date` | date |  |
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

Through the native Cerbo API, this operation is `GET /appointment_types` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-appointment-types.md) for the provider-specific parameters and requirements.

