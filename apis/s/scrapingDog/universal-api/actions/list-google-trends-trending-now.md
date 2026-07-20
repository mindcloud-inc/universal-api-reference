# ScrapingDog: List Google Trends Trending Now

Retrieves trending-now topics from Google Trends through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-google-trends-trending-now
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-google-trends-trending-now?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/list-google-trends-trending-now?${params}`, {
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
| `geo` | string | no | Geographic origin for trending-now results, such as US. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "trending_searches": {
        "active": true,
        "end_timestamp": "string",
        "id": [
          1
        ],
        "increase_percentage": 1,
        "search_volume": 1,
        "start_timestamp": 1,
        "title": "string",
        "trend_breakdown": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `trending_searches` | array<object> |  |
| `trending_searches.active` | boolean |  |
| `trending_searches.end_timestamp` | string |  |
| `trending_searches.id` | array<number> |  |
| `trending_searches.increase_percentage` | number |  |
| `trending_searches.search_volume` | number |  |
| `trending_searches.start_timestamp` | number |  |
| `trending_searches.title` | string |  |
| `trending_searches.trend_breakdown` | array<string> |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_trends/trending_now` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-google-trends-trending-now.md) for the provider-specific parameters and requirements.

