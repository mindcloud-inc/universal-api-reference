# Conveyor: List Interactions By Question

Retrieves interactions for a knowledge base question from Conveyor.

```
GET https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-interactions-by-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-interactions-by-question?connectionId=$CONNECTION_ID&limit=25&offset=0&questionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "questionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-interactions-by-question?${params}`, {
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
| `questionId` | string | yes | Knowledge base question identifier. |
| `createdAtStart` | date | no | Start of created-at date range. |
| `createdAtEnd` | date | no | End of created-at date range. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "interactions": [
        {
          "connection": {},
          "content": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "id": "string",
          "type": "string"
        }
      ],
      "page": 1,
      "per_page": 1,
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `interactions` | array<object> |  |
| `interactions[].connection` | object |  |
| `interactions[].content` | string |  |
| `interactions[].created_at` | date |  |
| `interactions[].email` | string |  |
| `interactions[].id` | string |  |
| `interactions[].type` | string |  |
| `page` | number |  |
| `per_page` | number |  |
| `total_pages` | number |  |

## Native endpoint

Through the native Conveyor API, this operation is `GET /v2/interactions/questions/:question_id` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-interactions-by-question.md) for the provider-specific parameters and requirements.

