# Zoho People: Get Attendance Entries

Retrieves attendance entries from Zoho People.

```
GET https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-attendance-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-attendance-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-attendance-entries?${params}`, {
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
| `employeeZohoId` | number | no | Optional Zoho employee ID. |
| `employeeEmailId` | string | no | Optional employee email identifier. |
| `employeeBiometricMapperId` | string | no | Optional employee biometric mapper identifier. |
| `employeeId` | string | no | Optional employee ID. |
| `fromDate` | string | no | Optional start date in the organization date format. |
| `toDate` | string | no | Optional end date in the organization date format. |
| `lastModifiedWithin` | number | no | Fetch entries created or updated within the last N minutes. |
| `groupEntriesByDate` | boolean | no | Group attendance entries by date. |
| `groupEntriesByEmployee` | boolean | no | Group attendance entries by employee. |
| `offset` | number | no | Start index for the attendance rows to fetch. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_by": "string",
      "created_time": "string",
      "employee": {
        "first_name": "Ava",
        "id": "string",
        "last_name": "Chen",
        "mail_id": "string",
        "zoho_id": "string"
      },
      "entry_id": "string",
      "is_break": true,
      "is_hourly_permission": true,
      "is_on_duty": true,
      "modified_by": "string",
      "modified_time": "string",
      "origin_day": "string",
      "punch_in": {
        "country": "string",
        "location": "string",
        "notes": "string",
        "punch": "string",
        "source": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_by` | string |  |
| `created_time` | string |  |
| `employee.first_name` | string |  |
| `employee.id` | string |  |
| `employee.last_name` | string |  |
| `employee.mail_id` | string |  |
| `employee.zoho_id` | string |  |
| `entry_id` | string |  |
| `is_break` | boolean |  |
| `is_hourly_permission` | boolean |  |
| `is_on_duty` | boolean |  |
| `modified_by` | string |  |
| `modified_time` | string |  |
| `origin_day` | string |  |
| `punch_in.country` | string |  |
| `punch_in.location` | string |  |
| `punch_in.notes` | string |  |
| `punch_in.punch` | string |  |
| `punch_in.source` | string |  |

## Native endpoint

Through the native Zoho People API, this operation is `GET /api/v3/attendance/entries` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attendance-entries.md) for the provider-specific parameters and requirements.

