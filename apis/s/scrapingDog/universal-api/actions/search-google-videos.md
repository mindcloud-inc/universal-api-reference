# ScrapingDog: Search Google Videos

Retrieves Google Videos search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-videos?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-videos?${params}`, {
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
| `query` | string | yes | Search query for Google Videos. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "current": "string",
        "next": "string",
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
      "video_results": {
        "displayed_link": "https://example.com",
        "link": "https://example.com",
        "rank": "string",
        "thumbnail": "string",
        "time": "string",
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
| `pagination` | object |  |
| `pagination.current` | string |  |
| `pagination.next` | string |  |
| `pagination.page_no` | object |  |
| `pagination.page_no.10` | string |  |
| `pagination.page_no.2` | string |  |
| `pagination.page_no.3` | string |  |
| `pagination.page_no.4` | string |  |
| `pagination.page_no.5` | string |  |
| `pagination.page_no.6` | string |  |
| `pagination.page_no.7` | string |  |
| `pagination.page_no.8` | string |  |
| `pagination.page_no.9` | string |  |
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
| `video_results` | array<object> |  |
| `video_results.displayed_link` | string |  |
| `video_results.link` | string |  |
| `video_results.rank` | string |  |
| `video_results.thumbnail` | string |  |
| `video_results.time` | string |  |
| `video_results.title` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_videos` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-videos.md) for the provider-specific parameters and requirements.

