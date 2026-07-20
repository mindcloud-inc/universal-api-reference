# Stackoverflow: List Featured Questions

Retrieves featured questions from Stackoverflow.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-featured-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-featured-questions?connectionId=$CONNECTION_ID&limit=25&offset=0&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-featured-questions?${params}`, {
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
| `site` | string | yes | API site parameter, for example stackoverflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer_count": 1,
      "content_license": "string",
      "creation_date": "2026-05-07T12:00:00.000Z",
      "is_answered": true,
      "last_activity_date": "2026-05-07T12:00:00.000Z",
      "link": "https://example.com",
      "question_id": 1,
      "score": 1,
      "tags": [
        "string"
      ],
      "title": "string",
      "view_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer_count` | number |  |
| `content_license` | string |  |
| `creation_date` | date |  |
| `is_answered` | boolean |  |
| `last_activity_date` | date |  |
| `link` | string |  |
| `question_id` | number |  |
| `score` | number |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `view_count` | number |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /questions/featured` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-featured-questions.md) for the provider-specific parameters and requirements.

