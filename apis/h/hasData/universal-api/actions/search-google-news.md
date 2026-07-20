# HasData: Search Google News

Retrieves Google News results from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-news?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-news?${params}`, {
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
| `q` | string | no | Free-text query to search on Google News. |
| `topicToken` | string | no | Google News topic token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "menuLinks": [
        {}
      ],
      "newsResults": [
        {}
      ],
      "relatedPublications": [
        {}
      ],
      "relatedTopics": [
        {}
      ],
      "requestMetadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `menuLinks` | array<object> |  |
| `newsResults` | array<object> |  |
| `relatedPublications` | array<object> |  |
| `relatedTopics` | array<object> |  |
| `requestMetadata` | object |  |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/google/news` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-news.md) for the provider-specific parameters and requirements.

