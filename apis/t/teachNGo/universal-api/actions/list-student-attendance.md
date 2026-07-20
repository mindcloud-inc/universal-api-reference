# Teach 'n Go: List Student Attendance

Retrieves student attendance records from Teach 'n Go.

```
GET https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-student-attendance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teach 'n Go `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-student-attendance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-student-attendance?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "absent": "string",
      "absentVolume": 1,
      "late": "string",
      "lateVolume": 1,
      "present": "string",
      "presentVolume": 1,
      "studentId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `absent` | string |  |
| `absentVolume` | number |  |
| `late` | string |  |
| `lateVolume` | number |  |
| `present` | string |  |
| `presentVolume` | number |  |
| `studentId` | number |  |

## Native endpoint

Through the native Teach 'n Go API, this operation is `POST /globalApis/students_attendance` (base URL `https://app.teachngo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-student-attendance.md) for the provider-specific parameters and requirements.

