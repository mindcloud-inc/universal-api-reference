# ScrapingDog: Get Google News Headlines

Retrieves Google News headlines through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-news-headlines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-news-headlines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-news-headlines?${params}`, {
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
| `query` | string | no | Query to filter Google News headline results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "news_results": {
        "authors": [
          "string"
        ],
        "date": "string",
        "link": "https://example.com",
        "rank": 1,
        "source": "string",
        "thumbnail": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `news_results` | array<object> |  |
| `news_results.authors` | array<string> |  |
| `news_results.date` | string |  |
| `news_results.link` | string |  |
| `news_results.rank` | number |  |
| `news_results.source` | string |  |
| `news_results.thumbnail` | string |  |
| `news_results.title` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_news/v2` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-news-headlines.md) for the provider-specific parameters and requirements.

