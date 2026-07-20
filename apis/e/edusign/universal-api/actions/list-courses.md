# Edusign: List Courses

Retrieves courses from Edusign.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-courses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-courses?${params}`, {
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
| `page` | string | no | Query param for pagination, starts at page "0" and displays 40 courses per page |
| `start` | string | no | Filter courses based on the course start date (format YYYY-MM-DD, ISO 8601) |
| `end` | string | no | Filter courses based on the course end date (format YYYY-MM-DD, ISO 8601). The difference between the start and end date must be 90 days maximum |
| `filters` | string | no | Filters must be separated by a comma ",". List of available filters : <br /> - locked : Retrieve all the locked courses <br /> - unlocked : Retrieve all the unlocked courses <br /> - absencessent : Retrieve all the absences send courses <br /> - absencesnotsent : Retrieve all the absences not send courses |
| `groupId` | string | no | Filter courses based on an array of groupIds to retrieve courses for specific groups Multiple groupIds can be provided, separated by commas (e.g., ?groupId=123,456,789). |
| `studentId` | string | no | Filter courses based on an array of studentIds to retrieve courses for specific students. Multiple studentIds can be provided, separated by commas (e.g., ?studentId=123,456,789). |
| `professorId` | string | no | Filter courses based on an array of professorIds to retrieve courses for specific professors. Multiple professorIds can be provided, separated by commas (e.g., ?studentId=123,456,789). |
| `trainingId` | string | no | Filter courses based on an array of trainingIds. Multiple trainingIds can be provided, separated by commas (e.g., ?trainingId=training123,training456). |
| `classroom` | string | no | Filter courses based on the classroom. |
| `creatorId` | string | no | Filter courses based on creatorId to retrieve courses for specific creatorId |
| `courseName` | string | no | Filter courses based on courseName to retrieve courses for specific courseName |
| `dateCreated` | string | no | Filter courses based on an array of two dates (start and end) (e.g., ?dateCreated=2024-08-01, 2024-08-02). |
| `infoStudents` | string | no | Returns detailed student information for the first course only. Values: "true" or "false" (default) Example: ?infoStudents=true Description: If "true", includes student details (first name, last name, email). If "false", only student states are returned. |
| `dateUpdated` | string | no | Filter courses based on an array of two dates (start and end) (e.g., ?dateUpdated=2024-08-01, 2024-08-02). |
| `professorSignature` | string | no | Filter courses based on professor's signature (true or false) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {
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
          "professorSignature": "string",
          "professorSignature2": "string",
          "professorSignature3": "string",
          "professorSignatureTimestamp": "string",
          "professorsPresences": [
            {
              "history": [
                "string"
              ],
              "priority": 1,
              "professorId": "string",
              "signature": "string"
            }
          ],
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
          "trainingInscriptionOptions": [
            "string"
          ],
          "zoom": 1
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | array<object> |  |
| `result[].absenceSent` | number |  |
| `result[].adminAnnotation` | string |  |
| `result[].annotation` | string |  |
| `result[].apiId` | string |  |
| `result[].apiType` | string |  |
| `result[].archivingCertificateUrl` | string |  |
| `result[].archivingId` | string |  |
| `result[].attendanceEnded` | number |  |
| `result[].attendanceListGenerated` | string |  |
| `result[].attendanceListGeneratedNologo` | string |  |
| `result[].classroom` | string |  |
| `result[].creatorId` | string |  |
| `result[].dateCreated` | string |  |
| `result[].dateUpdated` | string |  |
| `result[].description` | string |  |
| `result[].emailsAdded` | number |  |
| `result[].emailSignatureStudents` | string |  |
| `result[].end` | string |  |
| `result[].id` | string |  |
| `result[].inscriptionForms` | array<string> |  |
| `result[].locked` | boolean |  |
| `result[].maxStudents` | number |  |
| `result[].messages` | array<string> |  |
| `result[].metadata` | array<string> |  |
| `result[].metadataArchivingId` | string |  |
| `result[].name` | string |  |
| `result[].needStudentsSignature` | number |  |
| `result[].professor` | string |  |
| `result[].professor2` | string |  |
| `result[].professor3` | string |  |
| `result[].professorEmailHistory` | string |  |
| `result[].professorEmailHistory2` | string |  |
| `result[].professorSignature` | string |  |
| `result[].professorSignature2` | string |  |
| `result[].professorSignature3` | string |  |
| `result[].professorSignatureTimestamp` | string |  |
| `result[].professorsPresences` | array<object> |  |
| `result[].professorsPresences[].history` | array<string> |  |
| `result[].professorsPresences[].priority` | number |  |
| `result[].professorsPresences[].professorId` | string |  |
| `result[].professorsPresences[].signature` | string |  |
| `result[].readerId` | string |  |
| `result[].scannedAttendanceList` | string |  |
| `result[].schoolGroup` | array<string> |  |
| `result[].simpleSignature` | number |  |
| `result[].simpleSignaturePin` | string |  |
| `result[].start` | string |  |
| `result[].stateUpdate` | number |  |
| `result[].studentEmailReminder` | array<string> |  |
| `result[].studentInscriptionHash` | string |  |
| `result[].studentInscriptionSign` | number |  |
| `result[].students` | array<object> |  |
| `result[].students[].absenceId` | string |  |
| `result[].students[].comment` | string |  |
| `result[].students[].delay` | number |  |
| `result[].students[].excluded` | string |  |
| `result[].students[].state` | boolean |  |
| `result[].students[].studentId` | string |  |
| `result[].students[].timestamp` | string |  |
| `result[].surveyId` | string |  |
| `result[].surveyId2` | string |  |
| `result[].teacherSurvey` | string |  |
| `result[].teams` | number |  |
| `result[].teamsJson` | string |  |
| `result[].trainingId` | string |  |
| `result[].trainingInscriptionOptions` | array<string> |  |
| `result[].zoom` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/course` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-courses.md) for the provider-specific parameters and requirements.

