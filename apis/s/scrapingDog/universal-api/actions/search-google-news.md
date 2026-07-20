# ScrapingDog: Search Google News

Retrieves Google News search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-news?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-news?${params}`, {
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
| `query` | string | yes | Search query for Google News. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "news_results": {
        "favicon": "string",
        "imgSrc": "string",
        "lastUpdated": "string",
        "scrapingdog_link": "https://example.com",
        "snippet": "string",
        "source": "string",
        "title": "string",
        "url": "https://example.com"
      },
      "pagintion": {
        "current": "string",
        "page_no2": {
          "2": "string",
          "3": "string",
          "4": "string",
          "5": "string",
          "6": "string",
          "7": "string",
          "8": "string",
          "9": "string",
          "10": "string"
        },
        "previous": "string"
      },
      "scrapingdog_pagination": {
        "current": "string",
        "page_no": {
          "2": "string",
          "3": "string",
          "4": "string",
          "5": "string",
          "6": "string",
          "7": "string",
          "8": "string",
          "9": "string",
          "10": "string"
        }
      },
      "search_information": {
        "query_displayed": "string",
        "time_taken": "string",
        "url": "https://example.com"
      },
      "sub_articles": {
        "name": "Ava Chen",
        "news_results": {
          "favicon": "string",
          "scrapingdog_link": "https://example.com",
          "source": "string",
          "thumbnail": "string",
          "title": "string",
          "url": "https://example.com"
        }
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
| `news_results.favicon` | string |  |
| `news_results.imgSrc` | string |  |
| `news_results.lastUpdated` | string |  |
| `news_results.scrapingdog_link` | string |  |
| `news_results.snippet` | string |  |
| `news_results.source` | string |  |
| `news_results.title` | string |  |
| `news_results.url` | string |  |
| `pagintion` | object |  |
| `pagintion.current` | string |  |
| `pagintion.page_no2` | object |  |
| `pagintion.page_no2.10` | string |  |
| `pagintion.page_no2.2` | string |  |
| `pagintion.page_no2.3` | string |  |
| `pagintion.page_no2.4` | string |  |
| `pagintion.page_no2.5` | string |  |
| `pagintion.page_no2.6` | string |  |
| `pagintion.page_no2.7` | string |  |
| `pagintion.page_no2.8` | string |  |
| `pagintion.page_no2.9` | string |  |
| `pagintion.previous` | string |  |
| `scrapingdog_pagination` | object |  |
| `scrapingdog_pagination.current` | string |  |
| `scrapingdog_pagination.page_no` | object |  |
| `scrapingdog_pagination.page_no.10` | string |  |
| `scrapingdog_pagination.page_no.2` | string |  |
| `scrapingdog_pagination.page_no.3` | string |  |
| `scrapingdog_pagination.page_no.4` | string |  |
| `scrapingdog_pagination.page_no.5` | string |  |
| `scrapingdog_pagination.page_no.6` | string |  |
| `scrapingdog_pagination.page_no.7` | string |  |
| `scrapingdog_pagination.page_no.8` | string |  |
| `scrapingdog_pagination.page_no.9` | string |  |
| `search_information` | object |  |
| `search_information.query_displayed` | string |  |
| `search_information.time_taken` | string |  |
| `search_information.url` | string |  |
| `sub_articles` | array<object> |  |
| `sub_articles.name` | string |  |
| `sub_articles.news_results` | array<object> |  |
| `sub_articles.news_results.favicon` | string |  |
| `sub_articles.news_results.scrapingdog_link` | string |  |
| `sub_articles.news_results.source` | string |  |
| `sub_articles.news_results.thumbnail` | string |  |
| `sub_articles.news_results.title` | string |  |
| `sub_articles.news_results.url` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_news` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-news.md) for the provider-specific parameters and requirements.

