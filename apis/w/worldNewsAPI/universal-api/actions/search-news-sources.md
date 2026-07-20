# World News API: Search News Sources

Finds news sources in World News API by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/search-news-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/search-news-sources?connectionId=$CONNECTION_ID&name=cnn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "cnn"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/search-news-sources?${params}`, {
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
| `name` | string | yes | Source name query to match monitored news sources. Default: `cnn`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": 1,
      "sources": [
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
| `available` | number | Total number of matching monitored news sources. |
| `sources` | array<object> | Matching news sources. |

## Native endpoint

Through the native World News API API, this operation is `GET /search-news-sources` (base URL `https://api.worldnewsapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-news-sources.md) for the provider-specific parameters and requirements.

