# Stackoverflow: Search Question Excerpts

Finds question excerpts in Stackoverflow by search query.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/search-question-excerpts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/search-question-excerpts?connectionId=$CONNECTION_ID&limit=25&offset=0&site=string&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "site": "string",
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/search-question-excerpts?${params}`, {
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
| `q` | string | yes | Full-text search query to excerpt-match. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer_id": 1,
      "excerpt": "string",
      "item_type": "string",
      "question_id": 1,
      "question_score": 1,
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
| `answer_id` | number |  |
| `excerpt` | string |  |
| `item_type` | string |  |
| `question_id` | number |  |
| `question_score` | number |  |
| `score` | number |  |
| `tags` | array<string> |  |
| `title` | string |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /search/excerpts` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-question-excerpts.md) for the provider-specific parameters and requirements.

