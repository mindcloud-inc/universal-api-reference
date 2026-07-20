# QuestionPro Surveys: Get Survey Authentication



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-survey-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-survey-authentication?connectionId=$CONNECTION_ID&surveyId=13483869" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "13483869"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-survey-authentication?${params}`, {
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
| `surveyId` | number | yes | The QuestionPro survey ID. Example: `13483869`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folderID": 1,
      "name": "Ava Chen",
      "ownerID": 1,
      "surveyAuthentication": {},
      "surveyID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folderID` | number | The QuestionPro folder ID associated with the authentication configuration. |
| `name` | string | The survey name. |
| `ownerID` | number | The QuestionPro owner user ID. |
| `surveyAuthentication` | object | The survey authentication configuration. |
| `surveyID` | number | The QuestionPro survey ID. |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET surveys/:surveyId/authentication` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-authentication.md) for the provider-specific parameters and requirements.

