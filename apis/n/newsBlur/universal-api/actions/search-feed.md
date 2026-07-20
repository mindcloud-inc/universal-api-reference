# NewsBlur: Search Feed

Finds a feed in NewsBlur by website or RSS address.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/search-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/search-feed?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/search-feed?${params}`, {
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
| `address` | string | yes | RSS feed address or website address to search. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offset` | number | no | Offset for paging through feed search results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "feed_address": "string",
      "feed_link": "https://example.com",
      "feed_title": "string",
      "id": 1,
      "result": "string",
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
| `feed_address` | string | Feed RSS URL. |
| `feed_link` | string | Feed website URL. |
| `feed_title` | string | Feed title. |
| `id` | number | Feed ID. |
| `result` | string | Result status. |
| `user_id` | number | Authenticated NewsBlur user ID. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /rss_feeds/search_feed` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-feed.md) for the provider-specific parameters and requirements.

