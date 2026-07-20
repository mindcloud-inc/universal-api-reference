# QuestionPro Surveys: Get Question



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-question?connectionId=$CONNECTION_ID&questionId=158458653&surveyId=13483869" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionId": "158458653",
  "surveyId": "13483869"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-question?${params}`, {
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
      "address": {},
      "anchor": {},
      "answers": [
        {}
      ],
      "code": "string",
      "columns": [
        {}
      ],
      "email": {},
      "firstName": {},
      "lastName": {},
      "matrixType": "string",
      "mobileRendering": true,
      "notApplicableAnswer": true,
      "orderNumber": 1,
      "phone": {},
      "questionID": 1,
      "randomizedRows": true,
      "required": true,
      "rows": [
        {}
      ],
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object | Address field metadata for contact information questions when present. |
| `anchor` | object | Anchor labels and metadata for matrix-style questions when present. |
| `answers` | array<object> | Answer options when the question has fixed answers. |
| `code` | string | The provider-defined question code. |
| `columns` | array<object> | Matrix question columns when present. |
| `email` | object | Email field metadata for contact information questions when present. |
| `firstName` | object | First-name row metadata for contact information questions when present. |
| `lastName` | object | Last-name row metadata for contact information questions when present. |
| `matrixType` | string | The matrix rendering type when present. |
| `mobileRendering` | boolean | Whether the question is configured for mobile rendering when present. |
| `notApplicableAnswer` | boolean | Whether the question includes a not-applicable answer option when present. |
| `orderNumber` | number | The display order of the question within the survey. |
| `phone` | object | Phone field metadata for contact information questions when present. |
| `questionID` | number | The QuestionPro question ID. |
| `randomizedRows` | boolean | Whether matrix rows are randomized when present. |
| `required` | boolean | Whether the question is required. |
| `rows` | array<object> | Matrix or multi-row question rows when present. |
| `text` | string | The question text. |
| `type` | string | The QuestionPro question type. |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET surveys/:surveyId/questions/:questionId` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-question.md) for the provider-specific parameters and requirements.

