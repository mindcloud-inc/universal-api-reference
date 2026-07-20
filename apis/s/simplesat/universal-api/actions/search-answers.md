# Simplesat: Search Answers

Searches answers in Simplesat.

```
GET https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/search-answers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplesat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/search-answers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplesat/latest/actions/search-answers?${params}`, {
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
| `page` | number | no | The page number to retrieve |
| `pageSize` | number | no | The number of records per page |
| `startDate` | string | no |  |
| `endDate` | string | no |  |
| `operator` | string | no |  |
| `filters[]` | array<object> | no |  |

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

Through the native Simplesat API, this operation is `POST /api/v1/answers/search` (base URL `https://api.simplesat.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-answers.md) for the provider-specific parameters and requirements.

