# Timekit: Delete Project

Deletes an existing project from Timekit.

```
DELETE https://connect.mindcloud.co/v1/universal/timekit/latest/actions/delete-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/timekit/latest/actions/delete-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timekit/latest/actions/delete-project?${params}`, {
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
      "allow_conference": 1,
      "allow_double_bookings": true,
      "availability": {
        "buffer": "string",
        "closest_time_interval": "string",
        "from": "string",
        "ignore_all_day_events": true,
        "length": "string",
        "mode": "string",
        "to": "string"
      },
      "booking": {
        "description": "string",
        "graph": "string",
        "rescheduling_url": "https://example.com",
        "what": "string",
        "where": "string"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "customer_fields": {
        "email": {
          "format": "ava@example.com",
          "prefilled": "ava@example.com",
          "readonly": true,
          "required": true,
          "title": "ava@example.com"
        },
        "name": {
          "format": "Ava Chen",
          "prefilled": "Ava Chen",
          "readonly": true,
          "required": true,
          "title": "Ava Chen"
        }
      },
      "distance": 1,
      "enabled_email_notification": true,
      "id": "string",
      "latitude": "string",
      "longitude": "string",
      "meta": {
        "wizardRun": "string"
      },
      "name": "Ava Chen",
      "reservation_time": "string",
      "slug": "string",
      "ui": {
        "availability_view": "string",
        "localization": {
          "allocated_resource_prefix": "string",
          "submit_button": "string",
          "success_message": "string"
        },
        "show_credits": true,
        "time_date_format": "string"
      },
      "updated_at": "2026-05-07T12:00:00.000Z",
      "use_hours_from": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_conference` | number |  |
| `allow_double_bookings` | boolean |  |
| `availability.buffer` | string |  |
| `availability.closest_time_interval` | string |  |
| `availability.from` | string |  |
| `availability.ignore_all_day_events` | boolean |  |
| `availability.length` | string |  |
| `availability.mode` | string |  |
| `availability.to` | string |  |
| `booking.description` | string |  |
| `booking.graph` | string |  |
| `booking.rescheduling_url` | string |  |
| `booking.what` | string |  |
| `booking.where` | string |  |
| `created_at` | date |  |
| `customer_fields.email.format` | string |  |
| `customer_fields.email.prefilled` | string |  |
| `customer_fields.email.readonly` | boolean |  |
| `customer_fields.email.required` | boolean |  |
| `customer_fields.email.title` | string |  |
| `customer_fields.name.format` | string |  |
| `customer_fields.name.prefilled` | string |  |
| `customer_fields.name.readonly` | boolean |  |
| `customer_fields.name.required` | boolean |  |
| `customer_fields.name.title` | string |  |
| `distance` | number |  |
| `enabled_email_notification` | boolean |  |
| `id` | string |  |
| `latitude` | string |  |
| `longitude` | string |  |
| `meta.wizardRun` | string |  |
| `name` | string |  |
| `reservation_time` | string |  |
| `slug` | string |  |
| `ui.availability_view` | string |  |
| `ui.localization.allocated_resource_prefix` | string |  |
| `ui.localization.submit_button` | string |  |
| `ui.localization.success_message` | string |  |
| `ui.show_credits` | boolean |  |
| `ui.time_date_format` | string |  |
| `updated_at` | date |  |
| `use_hours_from` | string |  |

## Native endpoint

Through the native Timekit API, this operation is `DELETE /projects/:id` (base URL `https://api.timekit.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project.md) for the provider-specific parameters and requirements.

