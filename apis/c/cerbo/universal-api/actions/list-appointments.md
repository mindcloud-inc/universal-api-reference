# Cerbo: List Appointments

Retrieves appointment records from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-appointments?connectionId=$CONNECTION_ID&limit=25&offset=0&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-appointments?${params}`, {
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
| `startDate` | string | yes | Starting date of the date range. The start date should be formatted as `YYYY-MM-DD`. |
| `status` | string | no | Appointment status. If specified, results will be for only the given statuses. Valid statuses include `scheduled`, `confirmed`, `checked-in`, `in-room`, `cancelled`. Clinic custom statuses may also be used. |
| `endDate` | string | yes | Ending date of the date range. The end date should be formatted as `YYYY-MM-DD`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `providerId` | number | no | Provider identifier. If specified, results will be for only that provider. |
| `ptId` | number | no | Patient identifier. If specified, results will be for only that patient. |
| `includeCancelled` | string | no | If specified and not empty, results will include cancelled appointments. Any non-empty value is treated as true. |
| `includeWorkSchedule` | string | no | Include details about when a provider is set to work. Any non-empty value is treated as true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedby": 1,
      "appointment_location": "string",
      "appointment_note": "string",
      "appointment_status": "string",
      "appointment_type": "string",
      "associated_providers": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "datedeleted": "2026-05-07T12:00:00.000Z",
      "end_date_time": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "object": "string",
      "patient_details": {
        "dob": "2026-05-07T12:00:00.000Z",
        "email1": "ava@example.com",
        "first_name": "Ava",
        "id": "string",
        "last_name": "Chen",
        "middle_name": "Ava Chen",
        "object": "string",
        "sex": "string",
        "url_patient_details": "https://example.com"
      },
      "recurrance_group": "string",
      "recurrance_interval": 1,
      "recurrance_type": "string",
      "recurrance_value": "string",
      "start_date_time": "2026-05-07T12:00:00.000Z",
      "telemedicine": {
        "is_telemedicine": true,
        "telemedicine_url": "https://example.com"
      },
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedby` | number |  |
| `appointment_location` | string |  |
| `appointment_note` | string |  |
| `appointment_status` | string |  |
| `appointment_type` | string |  |
| `associated_providers` | array<object> |  |
| `created` | date |  |
| `datedeleted` | date |  |
| `end_date_time` | date |  |
| `id` | number |  |
| `object` | string |  |
| `patient_details` | object |  |
| `patient_details.dob` | date |  |
| `patient_details.email1` | string |  |
| `patient_details.first_name` | string |  |
| `patient_details.id` | string |  |
| `patient_details.last_name` | string |  |
| `patient_details.middle_name` | string |  |
| `patient_details.object` | string |  |
| `patient_details.sex` | string |  |
| `patient_details.url_patient_details` | string |  |
| `recurrance_group` | string |  |
| `recurrance_interval` | number |  |
| `recurrance_type` | string |  |
| `recurrance_value` | string |  |
| `start_date_time` | date |  |
| `telemedicine` | object |  |
| `telemedicine.is_telemedicine` | boolean |  |
| `telemedicine.telemedicine_url` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /appointments` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-appointments.md) for the provider-specific parameters and requirements.

