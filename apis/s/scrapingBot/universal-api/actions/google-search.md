# ScrapingBot: Google Search



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/google-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/google-search?connectionId=$CONNECTION_ID&q=best%20web%20scraping%20tools%202025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "best web scraping tools 2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/google-search?${params}`, {
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
| `q` | string | yes | Google search query. Example: `best web scraping tools 2025`. |
| `gl` | string | no | Country code for localized results, such as us or de. Example: `us`. |
| `hl` | string | no | Language code for localized results, such as en or es. Example: `en`. |
| `num` | number | no | Number of search results to return. Example: `10`. |
| `page` | number | no | Page number of the search results. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "duration": "string",
      "organic": [
        {}
      ],
      "peopleAlsoAsk": [
        {}
      ],
      "relatedSearches": [
        {}
      ],
      "searchParameters": {},
      "statusCode": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number | Credits consumed by the request. |
| `duration` | string | Provider execution duration in seconds. |
| `organic` | array<object> | Organic Google results. |
| `peopleAlsoAsk` | array<object> | People Also Ask entries when available. |
| `relatedSearches` | array<object> | Related Google searches when available. |
| `searchParameters` | object | Normalized search request metadata returned by ScrapingBot. |
| `statusCode` | number | HTTP status code reported by ScrapingBot. |
| `success` | boolean | Whether the provider request succeeded. |

## Native endpoint

Through the native ScrapingBot API, this operation is `POST /google` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/google-search.md) for the provider-specific parameters and requirements.

