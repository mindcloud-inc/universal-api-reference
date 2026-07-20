# Stackoverflow: Search Questions

Finds questions in Stackoverflow by search query.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/search-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/search-questions?connectionId=$CONNECTION_ID&limit=25&offset=0&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/search-questions?${params}`, {
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
| `site` | string | yes | Stack Exchange site parameter, for example stackoverflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer_count": 1,
      "is_answered": true,
      "link": "https://example.com",
      "question_id": 1,
      "score": 1,
      "tags": [
        "string"
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer_count` | number |  |
| `is_answered` | boolean |  |
| `link` | string |  |
| `question_id` | number |  |
| `score` | number |  |
| `tags` | array<string> |  |
| `title` | string |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /search` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-questions.md) for the provider-specific parameters and requirements.

