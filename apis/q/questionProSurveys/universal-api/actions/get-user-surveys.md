# QuestionPro Surveys: Get User Surveys



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-user-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-user-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=6358571" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "6358571"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-user-surveys?${params}`, {
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
| `userId` | number | yes | The QuestionPro user ID. Example: `6358571`. |

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

Through the native QuestionPro Surveys API, this operation is `GET users/:userId/surveys` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-user-surveys.md) for the provider-specific parameters and requirements.

