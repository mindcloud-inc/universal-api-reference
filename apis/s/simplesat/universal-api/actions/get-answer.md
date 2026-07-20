# Simplesat: Get Answer

Retrieves an answer from Simplesat.

```
GET https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/get-answer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/get-answer?connectionId=$CONNECTION_ID&answerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "answerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/get-answer?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `answerId` | string | yes | The ID of the answer to retrieve |

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
| `modified` | string |  |
| `published_as_testimonial` | boolean |  |
| `question` | object |  |
| `response_id` | number |  |
| `sentiment` | string |  |
| `survey` | object |  |

## Native endpoint

Through the native Simplesat API, this operation is `GET /api/v1/answers/:answer_id` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-answer.md) for the provider-specific parameters and requirements.

