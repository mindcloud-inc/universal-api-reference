# Zoho People: Add Attendance Entries

Creates attendance entries in Zoho People.

```
POST https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/add-attendance-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/add-attendance-entries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "punchDetails": "string",
  "datetimeFormat": "yyyy-MM-dd HH:mm:ss"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/add-attendance-entries', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "punchDetails": "string",
    "datetimeFormat": "yyyy-MM-dd HH:mm:ss"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `punchDetails` | string | yes | JSON array of attendance entries to add. |
| `datetimeFormat` | string | yes | Datetime format for the punch_details payload, for example yyyy-MM-dd HH:mm:ss. Default: `yyyy-MM-dd HH:mm:ss`. |
| `entriesTimezone` | string | no | Timezone of the source entries, such as a biometric device timezone. |
| `storageTimezone` | string | no | Timezone to store the attendance entries in Zoho People. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "empty_employee_ids": [
          "string"
        ],
        "error_information": [
          {}
        ],
        "maximum_entry_date": "string",
        "minimmun_entry_date": "string",
        "skipped_empolyee_info": [
          {}
        ],
        "success_count": 1,
        "total_count": 1
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.empty_employee_ids` | array<string> |  |
| `data.error_information` | array<object> |  |
| `data.maximum_entry_date` | string |  |
| `data.minimmun_entry_date` | string |  |
| `data.skipped_empolyee_info` | array<object> |  |
| `data.success_count` | number |  |
| `data.total_count` | number |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho People API, this operation is `POST /api/v3/attendance/entries` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-attendance-entries.md) for the provider-specific parameters and requirements.

