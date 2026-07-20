# Scrape do: Search Google

Finds Google search results with Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/search-google
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/search-google?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/search-google?${params}`, {
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
| `q` | string | yes | The Google search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bottom_ads": [
        {}
      ],
      "discussions_and_forums": [
        {}
      ],
      "navigation": [
        {}
      ],
      "organic_results": [
        {}
      ],
      "pagination": {},
      "related_questions": [
        {}
      ],
      "related_searches": [
        {}
      ],
      "search_information": {},
      "search_parameters": {},
      "top_ads": [
        {}
      ],
      "top_stories": [
        {}
      ],
      "video_results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bottom_ads` | array<object> | Ads shown below results. |
| `discussions_and_forums` | array<object> | Forum and discussion results. |
| `navigation` | array<object> | Google result navigation tabs. |
| `organic_results` | array<object> | Organic search results. |
| `pagination` | object | Pagination links and state. |
| `related_questions` | array<object> | People also ask entries. |
| `related_searches` | array<object> | Related search suggestions. |
| `search_information` | object | Search result metadata. |
| `search_parameters` | object | Echo of Google search request parameters. |
| `top_ads` | array<object> | Ads shown above results. |
| `top_stories` | array<object> | Top stories groups. |
| `video_results` | array<object> | Video result entries. |

## Native endpoint

Through the native Scrape do API, this operation is `GET /plugin/google/search` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google.md) for the provider-specific parameters and requirements.

