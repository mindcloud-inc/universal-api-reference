# ClassMarker: Update Question



```
PUT https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/update-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClassMarker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/update-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "questionId": 1,
  "question": "string",
  "questionType": "string",
  "categoryId": 1,
  "points": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/update-question', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "questionId": 1,
    "question": "string",
    "questionType": "string",
    "categoryId": 1,
    "points": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `questionId` | number | yes | Numeric ClassMarker question ID. |
| `question` | string | yes | Question text shown to exam takers. |
| `questionType` | string | yes | Writable ClassMarker question type: multiplechoice, multipleresponse, truefalse, or essay. |
| `categoryId` | number | yes | Numeric ClassMarker category ID that owns the question. |
| `points` | number | yes | Points awarded for a correct answer. |
| `randomAnswers` | boolean | no | Whether ClassMarker should randomize answer order for supported question types. |
| `options` | object | no | Options object keyed by letter (for example A, B, C) for supported question types. |
| `correctOptions[]` | array<string> | no | Option letters that are correct for the question type. |
| `gradeStyle` | string | no | Multiple response grading style: partial_with_deduction, partial_without_deduction, or off. |
| `correctFeedback` | string | no | Feedback shown for a correct answer. |
| `incorrectFeedback` | string | no | Feedback shown for an incorrect answer. |
| `verifyOnly` | boolean | no | Validate the request without updating the question. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": 1,
      "correctFeedback": "string",
      "correctOptions": [
        [
          "string"
        ]
      ],
      "gradeStyle": "string",
      "incorrectFeedback": "string",
      "lastUpdatedTimestamp": 1,
      "options": {},
      "points": "string",
      "question": "string",
      "questionId": 1,
      "questionType": "string",
      "randomAnswers": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number |  |
| `correctFeedback` | string |  |
| `correctOptions[]` | array<string> |  |
| `gradeStyle` | string |  |
| `incorrectFeedback` | string |  |
| `lastUpdatedTimestamp` | number |  |
| `options` | object |  |
| `points` | string |  |
| `question` | string |  |
| `questionId` | number |  |
| `questionType` | string |  |
| `randomAnswers` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native ClassMarker API, this operation is `PUT /v1/questions/{question_id}.json` (base URL `https://api.classmarker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-question.md) for the provider-specific parameters and requirements.

