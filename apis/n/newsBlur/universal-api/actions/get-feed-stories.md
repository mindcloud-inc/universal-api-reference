# NewsBlur: Get Feed Stories

Retrieves stories from a feed in NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-feed-stories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-feed-stories?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-feed-stories?${params}`, {
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
| `id` | number | yes | Feed ID to retrieve stories from. |
| `order` | string | no | Story order: newest or oldest. One of: `0`, `1`. |
| `readFilter` | string | no | Show all stories or only unread stories. One of: `0`, `1`. |
| `includeStoryContent` | boolean | no | Include story content in the response. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateFilterStart` | date | no | Only include stories published on or after this date in YYYY-MM-DD format. |
| `dateFilterEnd` | date | no | Only include stories published on or before this date in YYYY-MM-DD format. |
| `includeHidden` | boolean | no | Include hidden stories. |
| `query` | string | no | Search keyword or phrase in the feed. NewsBlur notes feed search is premium-only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "classifiers": {},
      "feed_address": "string",
      "feed_id": 1,
      "feed_title": "string",
      "result": "string",
      "stories": [
        {}
      ],
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticated` | boolean | Whether the session is authenticated. |
| `classifiers` | object | Feed intelligence classifiers. |
| `feed_address` | string | Feed RSS URL. |
| `feed_id` | number | Feed ID. |
| `feed_title` | string | Feed title. |
| `result` | string | Result status. |
| `stories` | array<object> | Stories returned for the feed. |
| `user_id` | number | Authenticated NewsBlur user ID. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /reader/feed/:id` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feed-stories.md) for the provider-specific parameters and requirements.

