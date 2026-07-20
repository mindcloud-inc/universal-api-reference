# Survicate: List Survey Questions

Retrieves questions from a specific Survicate survey.

```
GET https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-survey-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-survey-questions?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-survey-questions?${params}`, {
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
| `surveyId` | string | yes | The unique identifier of the survey. |
| `start` | string | no | The question identifier used for paginated results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answerChoices": {
        "content": "string",
        "id": 1
      },
      "columns": [
        "string"
      ],
      "fields": {
        "label": "string",
        "type": "string"
      },
      "id": 1,
      "introduction": "string",
      "question": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answerChoices` | array<object> | Available answer choices for supported choice-based question types. |
| `answerChoices.content` | string | Display text of an answer choice. |
| `answerChoices.id` | number | Unique identifier of an answer choice. |
| `columns` | array<string> | Matrix question columns when the question type is matrix. |
| `fields` | array<object> | Form field definitions when the question type is form. |
| `fields.label` | string | Label of a form field. |
| `fields.type` | string | Type of a form field. |
| `id` | number | Unique identifier of the question. |
| `introduction` | string | Introduction shown before the question, when present. |
| `question` | string | Text of the question as displayed to the respondent. |
| `type` | string | Question type. |

## Native endpoint

Through the native Survicate API, this operation is `GET /surveys/:survey_id/questions` (base URL `https://data-api.survicate.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-survey-questions.md) for the provider-specific parameters and requirements.

