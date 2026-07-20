# Simplesat: Update Response

Updates an existing response in Simplesat.

```
PUT https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/update-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/update-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "responseId": "string",
  "surveyId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/update-response', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "responseId": "string",
    "surveyId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | number | yes |  |
| `tags[]` | array<string> | no |  |
| `answers[]` | array<object> | no |  |
| `teamMembers[]` | array<object> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `responseId` | string | yes | The ID of the response to update |
| `ticket` | object | no |  |
| `customer` | object | no |  |

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
      "follow_up_answer": "string",
      "follow_up_answer_choice": "string",
      "follow_up_answer_choices": [
        "string"
      ],
      "follow_up_question": {},
      "id": 1,
      "question": {},
      "sentiment": "string"
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
| `follow_up_answer` | string |  |
| `follow_up_answer_choice` | string |  |
| `follow_up_answer_choices` | array<string> |  |
| `follow_up_question` | object |  |
| `id` | number |  |
| `question` | object |  |
| `sentiment` | string |  |

## Native endpoint

Through the native Simplesat API, this operation is `PUT /api/v1/responses/:response_id/update` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-response.md) for the provider-specific parameters and requirements.

