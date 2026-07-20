# World News API: Search News

Finds news articles in World News API by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/search-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/search-news?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/search-news?${params}`, {
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
| `authors` | string | no | Comma-separated list of author names to include. Accepts multiple values in one string, delimited by `,`. |
| `categories` | string | no | Comma-separated list of news categories to include. Accepts multiple values in one string, delimited by `,`. |
| `earliestPublishDate` | date | no | Earliest publish date/time to include. |
| `entities` | string | no | Comma-separated list of named entities to match. Accepts multiple values in one string, delimited by `,`. |
| `language` | string | no | Two-letter language code to restrict article language. |
| `latestPublishDate` | date | no | Latest publish date/time to include. |
| `locationFilter` | string | no | Location filter expression for nearby or regional news. |
| `maxSentiment` | number | no | Maximum sentiment score for returned articles. |
| `minSentiment` | number | no | Minimum sentiment score for returned articles. |
| `newsSources` | string | no | Comma-separated list of source names to include. Accepts multiple values in one string, delimited by `,`. |
| `number` | number | no | Maximum number of articles to return. |
| `offset` | number | no | Zero-based offset for paginating through search results. |
| `sort` | string | no | Field to sort the results by. |
| `sortDirection` | string | no | Sort direction for the selected sort field. |
| `sourceCountry` | string | no | Two-letter country code to restrict article sources. |
| `text` | string | no | Free-text query to search for matching news articles. |
| `textMatchIndexes` | boolean | no | Return match index metadata for the searched text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": 1,
      "news": [
        {}
      ],
      "number": 1,
      "offset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | number | Total number of matching news articles available. |
| `news` | array<object> | News articles matching the search filters. |
| `number` | number | Number of news articles returned in the response. |
| `offset` | number | Zero-based offset of the current search page. |

## Native endpoint

Through the native World News API API, this operation is `GET /search-news` (base URL `https://api.worldnewsapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-news.md) for the provider-specific parameters and requirements.

