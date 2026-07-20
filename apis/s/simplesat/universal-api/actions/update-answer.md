# Simplesat: Update Answer

Updates an existing answer in Simplesat.

```
PUT https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/update-answer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/update-answer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "answerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/update-answer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "answerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `choice` | string | no |  |
| `choices[]` | array<string> | no |  |
| `comment` | string | no |  |
| `followUpAnswer` | string | no |  |
| `followUpAnswerChoice` | string | no |  |
| `followUpAnswerChoices[]` | array<string> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `answerId` | string | yes | The ID of the answer to update |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choice": "string",
      "choice_label": "string",
      "choices": [
        "string"
      ],
      "comment": "string",
      "created": "string",
      "follow_up_answer": "string",
      "follow_up_answer_choice": "string",
      "follow_up_answer_choices": [
        "string"
      ],
      "id": 1,
      "modified": "string",
      "published_as_testimonial": true,
      "question": {},
      "response_id": 1,
      "sentiment": "string",
      "survey": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choice` | string |  |
| `choice_label` | string |  |
| `choices` | array<string> |  |
| `comment` | string |  |
| `created` | string |  |
| `follow_up_answer` | string |  |
| `follow_up_answer_choice` | string |  |
| `follow_up_answer_choices` | array<string> |  |
| `id` | number |  |
| `modified` | string |  |
| `published_as_testimonial` | boolean |  |
| `question` | object |  |
| `response_id` | number |  |
| `sentiment` | string |  |
| `survey` | object |  |

## Native endpoint

Through the native Simplesat API, this operation is `PUT /api/v1/answers/:answer_id` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-answer.md) for the provider-specific parameters and requirements.

