# Valyu: Search



```
GET https://connect.mindcloud.co/v1/universal/valyu/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Valyu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/valyu/latest/actions/search?connectionId=$CONNECTION_ID&query=Search%20across%20Valyu%20sources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "Search across Valyu sources"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/valyu/latest/actions/search?${params}`, {
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
| `query` | string | yes | The search query to execute. Example: `Search across Valyu sources`. |
| `max_num_results` | number | no | Maximum number of results to return. Example: `e.g. 10`. |
| `search_type` | string | no | Controls which data sources are searched. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "dataType": "string",
      "description": "string",
      "id": "string",
      "imageUrl": {},
      "length": 1,
      "price": 1,
      "publicationDate": "2026-05-07T12:00:00.000Z",
      "relevanceScore": 1,
      "source": "string",
      "sourceType": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `dataType` | string |  |
| `description` | string |  |
| `id` | string |  |
| `imageUrl` | object |  |
| `length` | number |  |
| `price` | number |  |
| `publicationDate` | date |  |
| `relevanceScore` | number |  |
| `source` | string |  |
| `sourceType` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Valyu API, this operation is `POST /search` (base URL `https://api.valyu.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

