# Conveyor: Answer Single Question

Answers a one-off question in Conveyor.

```
POST https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/answer-single-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/answer-single-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "question": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/answer-single-question', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "question": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `question` | string | yes | Question to answer. |
| `productLineIds` | string<string> | no | Product line identifiers to use as answer context. |
| `questionType` | string | no | Question type. |
| `multipleChoiceOptions[]` | array<string> | no | Multiple choice answer options. |
| `confidenceThreshold` | string | no | Minimum confidence threshold. |
| `email` | string | no | Requester email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "answer_confidence": "string",
      "id": "string",
      "question": "string",
      "structured_answer": {},
      "structured_answers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string |  |
| `answer_confidence` | string |  |
| `id` | string |  |
| `question` | string |  |
| `structured_answer` | object |  |
| `structured_answers` | array<object> |  |

## Native endpoint

Through the native Conveyor API, this operation is `POST /v2/single_question` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/answer-single-question.md) for the provider-specific parameters and requirements.

