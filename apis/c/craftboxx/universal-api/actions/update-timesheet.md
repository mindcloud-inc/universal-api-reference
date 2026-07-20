# Craftboxx: Update Timesheet

Updates a timesheet in Craftboxx.

```
PUT https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/update-timesheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Craftboxx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/update-timesheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timesheetId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/update-timesheet', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timesheetId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `end` | string | no | The timesheet end date or timestamp. |
| `start` | string | no | The timesheet start date or timestamp. |
| `timesheetId` | number | yes | The Craftboxx timesheet ID. |
| `workingTime` | number | no | The working time in minutes. |
| `breakTime` | number | no | The break time in minutes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "break_time": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "employee_id": 1,
      "end": "2026-05-07T12:00:00.000Z",
      "first_line": "string",
      "id": 1,
      "interfaces": [
        "string"
      ],
      "planner_changelog_url": "https://example.com",
      "planner_delete_url": "https://example.com",
      "planner_details_url": "https://example.com",
      "planner_edit_url": "https://example.com",
      "start": "2026-05-07T12:00:00.000Z",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "working_time": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `break_time` | number | Break time in minutes. |
| `created_at` | date | Creation timestamp. |
| `employee_id` | number | Employee ID. |
| `end` | date | End timestamp. |
| `first_line` | string | Primary display line. |
| `id` | number | Timesheet ID. |
| `interfaces` | array<string> | Available interface flags. |
| `planner_changelog_url` | string | Planner changelog URL. |
| `planner_delete_url` | string | Planner delete URL. |
| `planner_details_url` | string | Planner details URL. |
| `planner_edit_url` | string | Planner edit URL. |
| `start` | date | Start timestamp. |
| `updated_at` | date | Update timestamp. |
| `working_time` | number | Working time in minutes. |

## Native endpoint

Through the native Craftboxx API, this operation is `PUT timesheets/:timesheetId` (base URL `https://api.craftboxx.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-timesheet.md) for the provider-specific parameters and requirements.

