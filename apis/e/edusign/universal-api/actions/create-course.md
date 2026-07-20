# Edusign: Create Course

Creates a new course in Edusign.

```
POST https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "course": {},
  "course.name": "Ava Chen",
  "course.start": "string",
  "course.end": "string",
  "course.professor": "string",
  "course.needStudentsSignature": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-course', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "course": {},
    "course.name": "Ava Chen",
    "course.start": "string",
    "course.end": "string",
    "course.professor": "string",
    "course.needStudentsSignature": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `course` | object | yes |  |
| `course.name` | string | yes | Name of the course |
| `course.description` | string | no | Description of the course |
| `course.start` | string | yes | Start date of the course (ISO 8601 datetime) |
| `course.end` | string | yes | End date of the course (ISO 8601 datetime) |
| `course.professor` | string | yes | Professor ID |
| `course.professor2` | string | no | Professor 2 ID |
| `course.professor3` | string | no | Professor 3 ID |
| `course.classroom` | string | no | Classroom |
| `course.schoolGroup[]` | array<string> | no |  |
| `course.maxStudents` | number | no | Maximum number of students |
| `course.zoom` | boolean | no | Zoom course |
| `course.apiId` | string | no | API ID |
| `course.surveyId` | string | no | Survey Template ID |
| `course.surveyId2` | string | no | Survey Template ID 2. <br/> It's possible to send several surveys to students |
| `course.survey1AutomaticSendDate` | string | no | Survey 1 automatic send date (ISO 8601 datetime) |
| `course.survey2AutomaticSendDate` | string | no | Survey 2 automatic send date (ISO 8601 datetime) |
| `course.teacherSurvey` | string | no | Teacher survey ID |
| `course.trainingId` | string | no | Training ID |
| `course.needStudentsSignature` | boolean | yes | Need students signature |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "id": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `result.id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `POST /v1/course` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-course.md) for the provider-specific parameters and requirements.

