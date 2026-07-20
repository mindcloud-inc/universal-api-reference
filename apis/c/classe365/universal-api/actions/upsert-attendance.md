# Classe365: Upsert Attendance

Creates or updates attendance in Classe365.

```
POST https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-attendance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-attendance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-attendance', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `acds_id` | string | no | Academic session id. |
| `attendance_data` | string | no | JSON map of student attendance values. |
| `class_id` | string | no | Class id. |
| `date` | string | no | Attendance date in YYYY-MM-DD. |
| `section_id` | string | no | Section id. |
| `session_id` | string | no | Session id. |
| `subject_id` | string | no | Subject id. |
| `working` | string | no | 1 for working day. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "studentId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `date` | date |  |
| `status` | string |  |
| `studentId` | number |  |

## Native endpoint

Through the native Classe365 API, this operation is `POST /rest/manageAttendance` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-attendance.md) for the provider-specific parameters and requirements.

