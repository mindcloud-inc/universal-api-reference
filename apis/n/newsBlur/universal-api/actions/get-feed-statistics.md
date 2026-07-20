# NewsBlur: Get Feed Statistics

Retrieves feed statistics from NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-feed-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-feed-statistics?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-feed-statistics?${params}`, {
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
| `id` | number | yes | Feed ID for statistics. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "average_stories_per_month": 1,
      "feed_address": "string",
      "feed_id": 1,
      "feed_link": "https://example.com",
      "feed_title": "string",
      "num_subscribers": 1,
      "result": "string",
      "stories_last_month": 1,
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
| `average_stories_per_month` | number | Average monthly story count. |
| `feed_address` | string | Feed RSS URL. |
| `feed_id` | number | Feed ID. |
| `feed_link` | string | Feed website URL. |
| `feed_title` | string | Feed title. |
| `num_subscribers` | number | Subscriber count. |
| `result` | string | Result status. |
| `stories_last_month` | number | Stories published last month. |
| `user_id` | number | Authenticated NewsBlur user ID. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /rss_feeds/statistics/:id` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feed-statistics.md) for the provider-specific parameters and requirements.

