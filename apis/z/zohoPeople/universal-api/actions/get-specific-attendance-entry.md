# Zoho People: Get Specific Attendance Entry

Retrieves an attendance entry from Zoho People.

```
GET https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-specific-attendance-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-specific-attendance-entry?connectionId=$CONNECTION_ID&entryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-specific-attendance-entry?${params}`, {
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
| `entryId` | string | yes | Attendance entry ID. |
| `date` | string | no | Required only when the origin day does not fall within the current year. |

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
      },
      "punch_out": {
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
| `punch_out.country` | string |  |
| `punch_out.location` | string |  |
| `punch_out.notes` | string |  |
| `punch_out.punch` | string |  |
| `punch_out.source` | string |  |

## Native endpoint

Through the native Zoho People API, this operation is `GET /api/v3/attendance/entries/:entryId` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-specific-attendance-entry.md) for the provider-specific parameters and requirements.

