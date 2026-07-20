# Classe365: Enroll Student in Course

Enrolls a student in a course in Classe365.

```
POST https://connect.mindcloud.co/v1/universal/classe365/latest/actions/enroll-student-in-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/enroll-student-in-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classe365/latest/actions/enroll-student-in-course', {
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
| `class_id` | string | no | Class id. |
| `section_id` | string | no | Section id. |
| `status` | string | no | Enrollment status code, such as I for In Progress. |
| `student_id` | string | no | Student id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acdsId": 1,
      "classId": 1,
      "sectionId": 1,
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
| `acdsId` | number |  |
| `classId` | number |  |
| `sectionId` | number |  |
| `status` | string |  |
| `studentId` | number |  |

## Native endpoint

Through the native Classe365 API, this operation is `POST /rest/studentCourseEnroll` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enroll-student-in-course.md) for the provider-specific parameters and requirements.

