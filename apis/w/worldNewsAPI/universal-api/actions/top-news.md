# World News API: Top News

Retrieves top news headlines from World News API.

```
GET https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/top-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/top-news?connectionId=$CONNECTION_ID&language=en&sourceCountry=us" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "language": "en",
  "sourceCountry": "us"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/top-news?${params}`, {
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
| `date` | date | no | Date to retrieve top news for. |
| `headlinesOnly` | boolean | no | When true, return headline-only results. |
| `language` | string | yes | Two-letter language code for returned headlines. Default: `en`. |
| `maxNewsPerCluster` | number | no | Maximum number of articles to include in each top-news cluster. |
| `sourceCountry` | string | yes | Two-letter country code for the news source country. Default: `us`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "language": "string",
      "top_news": [
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
| `country` | string | Country code used for the top news response. |
| `language` | string | Language code used for the top news response. |
| `top_news` | array<object> | Clusters of top news articles for the selected country and language. |

## Native endpoint

Through the native World News API API, this operation is `GET /top-news` (base URL `https://api.worldnewsapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/top-news.md) for the provider-specific parameters and requirements.

