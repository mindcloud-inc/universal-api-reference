# Edusign: Get Survey By ID

Retrieves a survey from Edusign by ID.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-survey-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-survey-by-id?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-survey-by-id?${params}`, {
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
| `surveyId` | string | yes | Survey ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "anonymous": 1,
        "automaticSendDate": "string",
        "courseId": "string",
        "dateCreated": "string",
        "dateUpdated": "string",
        "hidden": 1,
        "id": "string",
        "message": "string",
        "name": "Ava Chen",
        "oldStudentAnswers": "string",
        "recipientIds": [
          "string"
        ],
        "recipientType": "string",
        "reminderEmailsNbSent": 1,
        "schoolId": "string",
        "sendToAbsents": 1,
        "studentAnswers": [
          {
            "answers": {},
            "completionDate": "string",
            "recipientType": "string",
            "studentId": "string"
          }
        ],
        "studentInscriptionHash": "string",
        "surveySent": 1,
        "template": "string",
        "templateId": "string",
        "trainingId": "string",
        "trainingSchedule": "string",
        "type": 1
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
| `result.anonymous` | number |  |
| `result.automaticSendDate` | string |  |
| `result.courseId` | string |  |
| `result.dateCreated` | string |  |
| `result.dateUpdated` | string |  |
| `result.hidden` | number |  |
| `result.id` | string |  |
| `result.message` | string |  |
| `result.name` | string |  |
| `result.oldStudentAnswers` | string |  |
| `result.recipientIds` | array<string> |  |
| `result.recipientType` | string |  |
| `result.reminderEmailsNbSent` | number |  |
| `result.schoolId` | string |  |
| `result.sendToAbsents` | number |  |
| `result.studentAnswers` | array<object> |  |
| `result.studentAnswers[].answers` | object |  |
| `result.studentAnswers[].completionDate` | string |  |
| `result.studentAnswers[].recipientType` | string |  |
| `result.studentAnswers[].studentId` | string |  |
| `result.studentInscriptionHash` | string |  |
| `result.surveySent` | number |  |
| `result.template` | string |  |
| `result.templateId` | string |  |
| `result.trainingId` | string |  |
| `result.trainingSchedule` | string |  |
| `result.type` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/surveys/:surveyId` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-by-id.md) for the provider-specific parameters and requirements.

