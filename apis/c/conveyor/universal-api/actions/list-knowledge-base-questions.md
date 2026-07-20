# Conveyor: List Knowledge Base Questions

Retrieves knowledge base questions from Conveyor.

```
GET https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-knowledge-base-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-knowledge-base-questions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-knowledge-base-questions?${params}`, {
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
| `status` | string | no | Knowledge base question verification status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "per_page": 1,
      "questions": [
        {
          "answer": "string",
          "id": "string",
          "question": "string",
          "status": "string"
        }
      ],
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number |  |
| `per_page` | number |  |
| `questions` | array<object> |  |
| `questions[].answer` | string |  |
| `questions[].id` | string |  |
| `questions[].question` | string |  |
| `questions[].status` | string |  |
| `total_pages` | number |  |

## Native endpoint

Through the native Conveyor API, this operation is `GET /v2/knowledge_base/questions` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-knowledge-base-questions.md) for the provider-specific parameters and requirements.

