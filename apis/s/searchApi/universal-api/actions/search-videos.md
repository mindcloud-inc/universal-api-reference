# SearchApi: Search Videos



```
GET https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-videos?connectionId=$CONNECTION_ID&q=scraping%20guides" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "scraping guides"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-videos?${params}`, {
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
| `q` | string | yes | Example: `scraping guides`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "relatedSearches": [
        {}
      ],
      "searchInformation": {},
      "searchMetadata": {},
      "searchParameters": {},
      "videos": [
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
| `relatedSearches` | array<object> |  |
| `searchInformation` | object |  |
| `searchMetadata` | object |  |
| `searchParameters` | object |  |
| `videos` | array<object> |  |

## Native endpoint

Through the native SearchApi API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-videos.md) for the provider-specific parameters and requirements.

