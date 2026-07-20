# Edusign: Update Course

Updates an existing course in Edusign.

```
PUT https://connect.mindcloud.co/v1/universal/edusign/latest/actions/update-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/update-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "course": {},
  "course.id": "string",
  "course.needStudentsSignature": true,
  "editSurveys": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/update-course', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "course": {},
    "course.id": "string",
    "course.needStudentsSignature": true,
    "editSurveys": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `course` | object | yes |  |
| `course.id` | string | yes | ID of the course |
| `course.name` | string | no | Name of the course |
| `course.description` | string | no | Description of the course |
| `course.start` | string | no | Start date of the course (ISO 8601 datetime) |
| `course.end` | string | no | End date of the course (ISO 8601 datetime) |
| `course.professor` | string | no | Professor ID at least one professor is required |
| `course.professor2` | string | no | Professor 2 ID |
| `course.professor3` | string | no | Professor 3 ID |
| `course.classroom` | string | no | Classroom |
| `course.schoolGroup[]` | array<string> | no |  |
| `course.surveyId` | string | no | Survey Template ID |
| `course.surveyId2` | string | no | Survey Template ID 2. <br/> It's possible to send several surveys to students |
| `course.teacherSurvey` | string | no |  |
| `course.survey1AutomaticSendDate` | string | no | Survey 1 automatic send date (ISO 8601 datetime) |
| `course.survey2AutomaticSendDate` | string | no | Survey 2 automatic send date (ISO 8601 datetime) |
| `course.teacherSurveyAutomaticSendDate` | string | no |  |
| `course.zoom` | boolean | no | Zoom course |
| `course.apiId` | string | no | API ID |
| `course.needStudentsSignature` | boolean | yes | Need students signature |
| `course.trainingId` | string | no | Training ID. Warning: if a course is already linked to a training and this field is set to null/empty, the course will be unlinked from that training |
| `editSurveys` | boolean | yes | Boolean query param (true/false), If true and a SURVEY_ID is provided, the survey will be erased and a new will be created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `PATCH /v1/course/` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-course.md) for the provider-specific parameters and requirements.

