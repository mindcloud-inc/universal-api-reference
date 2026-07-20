# Freshworks CRM: List Appointments

Retrieves all appointments from Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-appointments?${params}`, {
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
| `filter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointments": [
        [
          {}
        ]
      ],
      "meta": {
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointments[]` | array<object> | Appointments. |
| `appointments[].can_checkin` | boolean | Checkin availability. |
| `appointments[].can_checkin_checkout` | boolean | Checkin/checkout availability. |
| `appointments[].checkedin_at` | date | Checked-in timestamp. |
| `appointments[].checkedin_duration` | number | Check-in duration. |
| `appointments[].checkedout_at` | date | Checked-out timestamp. |
| `appointments[].checkedout_latitude` | number | Checked-out latitude. |
| `appointments[].checkedout_location` | string | Checked-out location. |
| `appointments[].checkedout_longitude` | number | Checked-out longitude. |
| `appointments[].conference_id` | number | Conference id. |
| `appointments[].created_at` | date | Created timestamp. |
| `appointments[].creater_id` | number | Creator id. |
| `appointments[].description` | string | Appointment description. |
| `appointments[].end_date` | date | End time. |
| `appointments[].from_date` | date | Start time. |
| `appointments[].has_multiple_emails` | boolean | Multiple email flag. |
| `appointments[].id` | number | Appointment identifier. |
| `appointments[].is_allday` | boolean | All-day flag. |
| `appointments[].latitude` | number | Latitude. |
| `appointments[].location` | string | Location. |
| `appointments[].longitude` | number | Longitude. |
| `appointments[].outcome_id` | number | Outcome identifier. |
| `appointments[].provider` | string | Provider. |
| `appointments[].targetables_with_email[]` | array<object> | Linked target records with email. |
| `appointments[].targetables_with_email[].id` | number | Target record id. |
| `appointments[].targetables_with_email[].name` | string | Target record name. |
| `appointments[].targetables_with_email[].type` | string | Target record type. |
| `appointments[].targetables[]` | array<object> | Linked target records. |
| `appointments[].targetables[].id` | number | Target record id. |
| `appointments[].targetables[].type` | string | Target record type. |
| `appointments[].time_zone` | string | Time zone. |
| `appointments[].title` | string | Appointment title. |
| `appointments[].updated_at` | date | Updated timestamp. |
| `meta.total` | number | Total appointments. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET /api/appointments` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-appointments.md) for the provider-specific parameters and requirements.

