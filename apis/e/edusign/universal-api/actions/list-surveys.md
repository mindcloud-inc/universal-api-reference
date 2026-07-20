# Edusign: List Surveys

Retrieves surveys from Edusign.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-surveys?${params}`, {
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
      "result": [
        {
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
          "reminderEmails": [
            {
              "dateSent": "ava@example.com",
              "nbSent": 1
            }
          ],
          "reminderEmailsNbSent": 1,
          "schoolId": "string",
          "sendToAbsents": 1,
          "showCorrectAnswersOnPdf": 1,
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
          "template": {
            "description": "string",
            "logoPosition": "string",
            "pages": [
              {
                "elements": [
                  {
                    "choices": [
                      {
                        "text": "string",
                        "value": "string"
                      }
                    ],
                    "name": "Ava Chen",
                    "title": "string",
                    "type": "string"
                  }
                ],
                "name": "Ava Chen"
              }
            ],
            "title": "string"
          },
          "templateId": "string",
          "trainingId": "string",
          "trainingSchedule": "string",
          "type": 1
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
| `result[].anonymous` | number |  |
| `result[].automaticSendDate` | string |  |
| `result[].courseId` | string |  |
| `result[].dateCreated` | string |  |
| `result[].dateUpdated` | string |  |
| `result[].hidden` | number |  |
| `result[].id` | string |  |
| `result[].message` | string |  |
| `result[].name` | string |  |
| `result[].oldStudentAnswers` | string |  |
| `result[].recipientIds` | array<string> |  |
| `result[].recipientType` | string |  |
| `result[].reminderEmails` | array<object> |  |
| `result[].reminderEmails[].dateSent` | string |  |
| `result[].reminderEmails[].nbSent` | number |  |
| `result[].reminderEmailsNbSent` | number |  |
| `result[].schoolId` | string |  |
| `result[].sendToAbsents` | number |  |
| `result[].showCorrectAnswersOnPdf` | number |  |
| `result[].studentAnswers` | array<object> |  |
| `result[].studentAnswers[].answers` | object |  |
| `result[].studentAnswers[].completionDate` | string |  |
| `result[].studentAnswers[].recipientType` | string |  |
| `result[].studentAnswers[].studentId` | string |  |
| `result[].studentInscriptionHash` | string |  |
| `result[].surveySent` | number |  |
| `result[].template` | object |  |
| `result[].template.description` | string |  |
| `result[].template.logoPosition` | string |  |
| `result[].template.pages` | array<object> |  |
| `result[].template.pages[].elements` | array<object> |  |
| `result[].template.pages[].elements[].choices` | array<object> |  |
| `result[].template.pages[].elements[].choices[].text` | string |  |
| `result[].template.pages[].elements[].choices[].value` | string |  |
| `result[].template.pages[].elements[].name` | string |  |
| `result[].template.pages[].elements[].title` | string |  |
| `result[].template.pages[].elements[].type` | string |  |
| `result[].template.pages[].name` | string |  |
| `result[].template.title` | string |  |
| `result[].templateId` | string |  |
| `result[].trainingId` | string |  |
| `result[].trainingSchedule` | string |  |
| `result[].type` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/surveys` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

