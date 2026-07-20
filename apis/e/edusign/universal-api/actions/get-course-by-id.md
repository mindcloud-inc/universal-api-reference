# Edusign: Get Course By ID

Retrieves a course from Edusign by ID.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-course-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-course-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-course-by-id?${params}`, {
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
| `id` | string | yes | Course id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "absenceSent": 1,
        "adminAnnotation": "string",
        "annotation": "string",
        "apiId": "string",
        "apiType": "string",
        "archivingCertificateUrl": "https://example.com",
        "archivingId": "string",
        "attendanceEnded": 1,
        "attendanceListGenerated": "string",
        "attendanceListGeneratedNologo": "string",
        "classroom": "string",
        "creatorId": "string",
        "dateCreated": "string",
        "dateUpdated": "string",
        "description": "string",
        "emailsAdded": 1,
        "emailSignatureStudents": "ava@example.com",
        "end": "string",
        "id": "string",
        "idx": 1,
        "inscriptionForms": [
          "string"
        ],
        "locked": true,
        "maxStudents": 1,
        "messages": [
          "string"
        ],
        "metadata": [
          "string"
        ],
        "metadataArchivingId": "string",
        "name": "Ava Chen",
        "needStudentsSignature": 1,
        "professor": "string",
        "professor2": "string",
        "professor3": "string",
        "professorEmailHistory": "ava@example.com",
        "professorEmailHistory2": "ava@example.com",
        "professorEmailHistory3": "ava@example.com",
        "professorSignature": "string",
        "professorSignature2": "string",
        "professorSignature3": "string",
        "professorSignatureTimestamp": "string",
        "readerId": "string",
        "scannedAttendanceList": "string",
        "schoolGroup": [
          "string"
        ],
        "simpleSignature": 1,
        "simpleSignaturePin": "string",
        "start": "string",
        "stateUpdate": 1,
        "studentEmailReminder": [
          "ava@example.com"
        ],
        "studentInscriptionHash": "string",
        "studentInscriptionSign": 1,
        "students": [
          {
            "absenceId": "string",
            "comment": "string",
            "delay": 1,
            "excluded": "string",
            "state": true,
            "studentId": "string",
            "timestamp": "string"
          }
        ],
        "surveyId": "string",
        "surveyId2": "string",
        "teacherSurvey": "string",
        "teams": 1,
        "teamsJson": "string",
        "trainingId": "string",
        "zoom": 1
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
| `result.absenceSent` | number |  |
| `result.adminAnnotation` | string |  |
| `result.annotation` | string |  |
| `result.apiId` | string |  |
| `result.apiType` | string |  |
| `result.archivingCertificateUrl` | string |  |
| `result.archivingId` | string |  |
| `result.attendanceEnded` | number |  |
| `result.attendanceListGenerated` | string |  |
| `result.attendanceListGeneratedNologo` | string |  |
| `result.classroom` | string |  |
| `result.creatorId` | string |  |
| `result.dateCreated` | string |  |
| `result.dateUpdated` | string |  |
| `result.description` | string |  |
| `result.emailsAdded` | number |  |
| `result.emailSignatureStudents` | string |  |
| `result.end` | string |  |
| `result.id` | string |  |
| `result.idx` | number |  |
| `result.inscriptionForms` | array<string> |  |
| `result.locked` | boolean |  |
| `result.maxStudents` | number |  |
| `result.messages` | array<string> |  |
| `result.metadata` | array<string> |  |
| `result.metadataArchivingId` | string |  |
| `result.name` | string |  |
| `result.needStudentsSignature` | number |  |
| `result.professor` | string |  |
| `result.professor2` | string |  |
| `result.professor3` | string |  |
| `result.professorEmailHistory` | string |  |
| `result.professorEmailHistory2` | string |  |
| `result.professorEmailHistory3` | string |  |
| `result.professorSignature` | string |  |
| `result.professorSignature2` | string |  |
| `result.professorSignature3` | string |  |
| `result.professorSignatureTimestamp` | string |  |
| `result.readerId` | string |  |
| `result.scannedAttendanceList` | string |  |
| `result.schoolGroup` | array<string> |  |
| `result.simpleSignature` | number |  |
| `result.simpleSignaturePin` | string |  |
| `result.start` | string |  |
| `result.stateUpdate` | number |  |
| `result.studentEmailReminder` | array<string> |  |
| `result.studentInscriptionHash` | string |  |
| `result.studentInscriptionSign` | number |  |
| `result.students` | array<object> |  |
| `result.students[].absenceId` | string |  |
| `result.students[].comment` | string |  |
| `result.students[].delay` | number |  |
| `result.students[].excluded` | string |  |
| `result.students[].state` | boolean |  |
| `result.students[].studentId` | string |  |
| `result.students[].timestamp` | string |  |
| `result.surveyId` | string |  |
| `result.surveyId2` | string |  |
| `result.teacherSurvey` | string |  |
| `result.teams` | number |  |
| `result.teamsJson` | string |  |
| `result.trainingId` | string |  |
| `result.zoom` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/course/:id` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-course-by-id.md) for the provider-specific parameters and requirements.

