# Cloro: Extract Google News



```
POST https://connect.mindcloud.co/v1/universal/cloro/latest/actions/extract-google-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloro/latest/actions/extract-google-news" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloro/latest/actions/extract-google-news', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country` | string | no | ISO 3166-1 alpha-2 country code for localized news results. |
| `device` | string | no | Device type for news results. |
| `query` | string | yes | The search query to execute on Google News. |
| `pages` | number | no | Number of news results pages to scrape. |
| `include` | object | no | Optional flags for additional Google News response data. |
| `include.html` | boolean | no | Include raw HTML response URLs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "newsResults": [
          {
            "date": "string",
            "link": "https://example.com",
            "page": 1,
            "position": 1,
            "snippet": "string",
            "source": "string",
            "thumbnail": "string",
            "title": "string"
          }
        ]
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.newsResults[].date` | string |  |
| `result.newsResults[].link` | string |  |
| `result.newsResults[].page` | number |  |
| `result.newsResults[].position` | number |  |
| `result.newsResults[].snippet` | string |  |
| `result.newsResults[].source` | string |  |
| `result.newsResults[].thumbnail` | string |  |
| `result.newsResults[].title` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Cloro API, this operation is `POST /v1/monitor/google/news` (base URL `https://api.cloro.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-google-news.md) for the provider-specific parameters and requirements.

