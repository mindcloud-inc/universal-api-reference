# QuestionPro Surveys: Get Survey



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-survey?connectionId=$CONNECTION_ID&surveyId=1234567" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1234567"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-survey?${params}`, {
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
| `surveyId` | number | yes | The QuestionPro survey ID. Example: `1234567`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abbs": true,
      "completedResponses": 1,
      "completedText": "string",
      "creationDate": "string",
      "expiryDate": "string",
      "folderID": 1,
      "hasScoringLogic": true,
      "inactiveText": "string",
      "lastResponseReceived": "string",
      "logoUrl": "https://example.com",
      "modifiedDate": "string",
      "name": "Ava Chen",
      "ownerID": 1,
      "quotaOverlimitText": "string",
      "responseQuota": 1,
      "saveAndContinue": true,
      "startedResponses": 1,
      "status": "string",
      "surveyFinishMode": 1,
      "surveyID": 1,
      "surveyLanguages": [
        {}
      ],
      "terminatedResponses": 1,
      "terminatedText": "string",
      "thankYouMessage": "string",
      "url": "https://example.com",
      "viewedResponses": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abbs` | boolean |  |
| `completedResponses` | number |  |
| `completedText` | string |  |
| `creationDate` | string |  |
| `expiryDate` | string |  |
| `folderID` | number |  |
| `hasScoringLogic` | boolean |  |
| `inactiveText` | string |  |
| `lastResponseReceived` | string |  |
| `logoUrl` | string |  |
| `modifiedDate` | string |  |
| `name` | string |  |
| `ownerID` | number |  |
| `quotaOverlimitText` | string |  |
| `responseQuota` | number |  |
| `saveAndContinue` | boolean |  |
| `startedResponses` | number |  |
| `status` | string |  |
| `surveyFinishMode` | number |  |
| `surveyID` | number |  |
| `surveyLanguages` | array<object> |  |
| `terminatedResponses` | number |  |
| `terminatedText` | string |  |
| `thankYouMessage` | string |  |
| `url` | string |  |
| `viewedResponses` | number |  |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET surveys/:surveyId` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey.md) for the provider-specific parameters and requirements.

