# Money Talks News: List Global Comments Feed Items



```
GET https://connect.mindcloud.co/v1/universal/moneyTalksNews/latest/actions/list-global-comments-feed-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Money Talks News `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moneyTalksNews/latest/actions/list-global-comments-feed-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moneyTalksNews/latest/actions/list-global-comments-feed-items?${params}`, {
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
      "pubDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string | RSS author value when present. |
| `description` | string | RSS comment body or excerpt. |
| `guid` | string | Unique RSS comment identifier. |
| `link` | string | Canonical URL for the RSS comment item. |
| `pubDate` | date | RSS publication date. |
| `title` | string | RSS comment item title. |

## Native endpoint

Through the native Money Talks News API, this operation is `GET /comments/feed/` (base URL `https://www.moneytalksnews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-global-comments-feed-items.md) for the provider-specific parameters and requirements.

