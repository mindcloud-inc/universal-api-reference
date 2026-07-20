# Dev.to: List My Articles

Lists the authenticated user's published Dev.to articles.

```
GET https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-my-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-my-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-my-articles?${params}`, {
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
      "description": "string",
      "id": 1,
      "path": "string",
      "published": true,
      "published_at": "2026-05-07T12:00:00.000Z",
      "tag_list": [
        "string"
      ],
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
| `description` | string |  |
| `id` | number |  |
| `path` | string |  |
| `published` | boolean |  |
| `published_at` | date |  |
| `tag_list` | array<string> |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Dev.to API, this operation is `GET /articles/me` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-my-articles.md) for the provider-specific parameters and requirements.

