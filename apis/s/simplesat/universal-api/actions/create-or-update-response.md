# Simplesat: Create or Update Response

Creates or updates a response in Simplesat.

```
POST https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/create-or-update-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/create-or-update-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/create-or-update-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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

Through the native Simplesat API, this operation is `POST /api/v1/responses/create-or-update` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-response.md) for the provider-specific parameters and requirements.

