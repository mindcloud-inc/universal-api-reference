# Money Talks News: List Search Feed Items



```
GET https://connect.mindcloud.co/v1/universal/moneyTalksNews/latest/actions/list-search-feed-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Money Talks News `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moneyTalksNews/latest/actions/list-search-feed-items?connectionId=$CONNECTION_ID&searchTerm=savings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchTerm": "savings"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moneyTalksNews/latest/actions/list-search-feed-items?${params}`, {
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
| `searchTerm` | string | yes | Search term segment used in the Money Talks News RSS search feed URL. Example: `savings`. |

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
| `description` | string | RSS item description or excerpt. |
| `guid` | string | Unique RSS item identifier. |
| `link` | string | Canonical URL for the RSS item. |
| `pubDate` | date | RSS publication date. |
| `title` | string | RSS item title. |

## Native endpoint

Through the native Money Talks News API, this operation is `GET /search/:searchTerm/feed/rss2/` (base URL `https://www.moneytalksnews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-search-feed-items.md) for the provider-specific parameters and requirements.

