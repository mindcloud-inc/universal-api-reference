# Invision Community: Search Content



```
GET https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/search-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invision Community `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/search-content?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/search-content?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "authorUrl": "https://example.com",
      "container": "string",
      "containerUrl": "https://example.com",
      "content": "string",
      "itemId": 1,
      "itemUrl": "https://example.com",
      "objectId": 1,
      "objectUrl": "https://example.com",
      "page": 1,
      "perPage": 1,
      "results": [
        {}
      ],
      "title": "string",
      "totalPages": 1,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `authorUrl` | string |  |
| `container` | string |  |
| `containerUrl` | string |  |
| `content` | string |  |
| `itemId` | number |  |
| `itemUrl` | string |  |
| `objectId` | number |  |
| `objectUrl` | string |  |
| `page` | number |  |
| `perPage` | number |  |
| `results` | array<object> |  |
| `title` | string |  |
| `totalPages` | number |  |
| `totalResults` | number |  |

## Native endpoint

Through the native Invision Community API, this operation is `GET /core/search` (base URL `{{credentials.communityBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-content.md) for the provider-specific parameters and requirements.

