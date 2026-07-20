# BC Gov News: List Finance News

Retrieves finance announcements from BC Gov News.

```
GET https://connect.mindcloud.co/v1/universal/bCGovNews/latest/actions/list-finance-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BC Gov News `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bCGovNews/latest/actions/list-finance-news?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bCGovNews/latest/actions/list-finance-news?${params}`, {
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
      "category": "string",
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
| `category` | string | Feed category or ministry. |
| `description` | string | Short release summary. |
| `guid` | string | Stable RSS entry identifier. |
| `link` | string | Release URL. |
| `pubDate` | date | RSS publication date. |
| `title` | string | Release title. |

## Native endpoint

Through the native BC Gov News API, this operation is `GET /ministries/finance/feed` (base URL `https://news.gov.bc.ca`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-finance-news.md) for the provider-specific parameters and requirements.

