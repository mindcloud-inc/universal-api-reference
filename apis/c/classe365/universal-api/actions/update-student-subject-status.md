# Classe365: Update Student Subject Status

Updates a student's subject status in Classe365.

```
PUT https://connect.mindcloud.co/v1/universal/classe365/latest/actions/update-student-subject-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/update-student-subject-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classe365/latest/actions/update-student-subject-status', {
  method: 'PUT',
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
| `status` | string | no | Enrollment status code. |
| `student_id` | string | no | Student id. |
| `subject_id` | string | no | Subject id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "studentId": 1,
      "subjectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `studentId` | number |  |
| `subjectId` | number |  |

## Native endpoint

Through the native Classe365 API, this operation is `POST /rest/studentSubjectStatusUpdate` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-student-subject-status.md) for the provider-specific parameters and requirements.

