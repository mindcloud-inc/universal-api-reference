# SerpApi: Search Google Images

Retrieves Google image results from SerpApi.

```
GET https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/search-google-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SerpApi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/search-google-images?connectionId=$CONNECTION_ID&limit=25&offset=0&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serpApi/latest/actions/search-google-images?${params}`, {
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
| `q` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "link": "https://example.com",
      "source": "string",
      "thumbnail": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | string |  |
| `source` | string |  |
| `thumbnail` | string |  |
| `title` | string |  |

## Native endpoint

Through the native SerpApi API, this operation is `GET /search.json` (base URL `https://serpapi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-google-images.md) for the provider-specific parameters and requirements.

