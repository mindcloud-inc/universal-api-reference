# Hacker News: Get Item

Retrieves an item from Hacker News.

```
GET https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hacker News `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-item?connectionId=$CONNECTION_ID&id=47702791" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "47702791"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-item?${params}`, {
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
| `id` | number | yes | Numeric Hacker News item ID. Default: `47702791`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "by": "string",
      "dead": true,
      "deleted": true,
      "descendants": 1,
      "id": 1,
      "kids": [
        1
      ],
      "parent": 1,
      "parts": [
        1
      ],
      "poll": 1,
      "score": 1,
      "text": "string",
      "time": 1,
      "title": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `by` | string | Username of the item author. |
| `dead` | boolean | Whether the item is dead. |
| `deleted` | boolean | Whether the item is deleted. |
| `descendants` | number | Total comment count for stories or polls. |
| `id` | number | Unique Hacker News item ID. |
| `kids` | array<number> | Child comment IDs in ranked order. |
| `parent` | number | Parent item ID for comments. |
| `parts` | array<number> | Poll option item IDs for polls. |
| `poll` | number | Associated poll ID for poll options. |
| `score` | number | Story score or poll option votes. |
| `text` | string | HTML body for comments, stories, or polls. |
| `time` | number | Unix timestamp when the item was created. |
| `title` | string | Title for stories, polls, or jobs. |
| `type` | string | Item type: job, story, comment, poll, or pollopt. |
| `url` | string | Linked URL for story items. |

## Native endpoint

Through the native Hacker News API, this operation is `GET /item/:id.json` (base URL `https://hacker-news.firebaseio.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

