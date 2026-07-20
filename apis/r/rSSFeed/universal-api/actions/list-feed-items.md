# RSS Feed: List Feed Items

Retrieves items from the configured RSS feed.

```
GET https://connect.mindcloud.co/v1/universal/rSSFeed/latest/actions/list-feed-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RSS Feed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rSSFeed/latest/actions/list-feed-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rSSFeed/latest/actions/list-feed-items?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "description": "string",
      "guid": "string",
      "link": "https://example.com",
      "pubDate": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string | Author reported by the feed when available. |
| `description` | string | Item description or content snippet from the feed. |
| `guid` | string | Unique identifier for the RSS item. |
| `link` | string | Canonical URL for the RSS item. |
| `pubDate` | string | Publication date reported by the feed. |
| `title` | string | Title of the RSS item. |

## Native endpoint

Through the native RSS Feed API, this operation is `GET {{credentials.feedUrl}}` (base URL `{{credentials.feedUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-feed-items.md) for the provider-specific parameters and requirements.

