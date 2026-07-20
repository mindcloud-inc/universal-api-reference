# QuestionPro Surveys: Get Folder Surveys



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-folder-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-folder-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=6358571&folderId=6773259" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "6358571",
  "folderId": "6773259"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-folder-surveys?${params}`, {
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
| `folderId` | number | yes | The QuestionPro folder ID. Example: `6773259`. |

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
| `abbs` | boolean | Whether ABBS is enabled. |
| `completedResponses` | number | The completed response count. |
| `completedText` | string | The completed text shown after submission. |
| `creationDate` | string | The survey creation date. |
| `expiryDate` | string | The survey expiry date. |
| `folderID` | number | The QuestionPro folder ID. |
| `hasScoringLogic` | boolean | Whether scoring logic is enabled. |
| `inactiveText` | string | The message shown when the survey is inactive. |
| `lastResponseReceived` | string | The timestamp of the last received response. |
| `logoUrl` | string | The survey logo URL. |
| `modifiedDate` | string | The survey last modified date. |
| `name` | string | The survey name. |
| `ownerID` | number | The QuestionPro owner user ID. |
| `quotaOverlimitText` | string | The message shown when quota is exceeded. |
| `responseQuota` | number | The survey response quota. |
| `saveAndContinue` | boolean | Whether save-and-continue is enabled. |
| `startedResponses` | number | The started response count. |
| `status` | string | The survey status. |
| `surveyFinishMode` | number | The survey finish mode. |
| `surveyID` | number | The QuestionPro survey ID. |
| `surveyLanguages` | array<object> | The survey languages. |
| `terminatedResponses` | number | The terminated response count. |
| `terminatedText` | string | The terminated text shown to screened-out respondents. |
| `thankYouMessage` | string | The survey thank-you message. |
| `url` | string | The survey URL. |
| `viewedResponses` | number | The viewed response count. |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET users/:userId/folders/:folderId/surveys` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-folder-surveys.md) for the provider-specific parameters and requirements.

