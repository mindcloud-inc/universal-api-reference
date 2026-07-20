# Teach 'n Go: Enroll Student in Class

Enrolls a student in a Teach 'n Go class.

```
POST https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/enroll-student-in-class
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teach 'n Go `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/enroll-student-in-class" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseId": "string",
  "studentId": "string",
  "enrolmentDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/enroll-student-in-class', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseId": "string",
    "studentId": "string",
    "enrolmentDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseId` | string | yes | The class or course ID to enrol the student into. |
| `studentId` | string | yes | The existing student ID to enrol. |
| `enrolmentDate` | date | yes | The enrolment date in YYYY-MM-DD format. |
| `unenrolmentDate` | date | no | The optional unenrolment date in YYYY-MM-DD format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Teach 'n Go API returns.

## Native endpoint

Through the native Teach 'n Go API, this operation is `POST /api/enrollclass` (base URL `https://app.teachngo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enroll-student-in-class.md) for the provider-specific parameters and requirements.

