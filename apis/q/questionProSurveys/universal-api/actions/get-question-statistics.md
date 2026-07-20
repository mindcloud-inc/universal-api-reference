# QuestionPro Surveys: Get Question Statistics



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-question-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-question-statistics?connectionId=$CONNECTION_ID&questionId=158458653&surveyId=13483869" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionId": "158458653",
  "surveyId": "13483869"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-question-statistics?${params}`, {
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
      "questions": [
        {}
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `questions` | array<object> |  |
| `title` | string |  |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `POST surveys/:surveyId/questions/:questionId/analytics` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-question-statistics.md) for the provider-specific parameters and requirements.

