# QuestionPro Surveys: Get Answers



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-answers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-answers?connectionId=$CONNECTION_ID&limit=25&offset=0&questionId=158458653&surveyId=13483869" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "questionId": "158458653",
  "surveyId": "13483869"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-answers?${params}`, {
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
| `questionId` | number | yes | The QuestionPro question ID. Example: `158458653`. |
| `surveyId` | number | yes | The QuestionPro survey ID. Example: `13483869`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answerID": 1,
      "excludeRandomization": true,
      "hasNA": true,
      "hasOther": true,
      "orderNumber": 1,
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerID` | number | The QuestionPro answer ID. |
| `excludeRandomization` | boolean | Whether this answer is excluded from randomization. |
| `hasNA` | boolean | Whether this answer represents a not-applicable option. |
| `hasOther` | boolean | Whether this answer captures free-form other text. |
| `orderNumber` | number | The display order of the answer option. |
| `text` | string | The answer text. |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET surveys/:surveyId/questions/:questionId/answers` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-answers.md) for the provider-specific parameters and requirements.

