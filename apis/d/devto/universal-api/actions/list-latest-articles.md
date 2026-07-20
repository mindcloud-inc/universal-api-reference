# Dev.to: List Latest Articles

Lists published Dev.to articles sorted by newest publish date.

```
GET https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-latest-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-latest-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-latest-articles?${params}`, {
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
      "organization": {},
      "path": "string",
      "published_timestamp": "2026-05-07T12:00:00.000Z",
      "tag_list": [
        "string"
      ],
      "title": "string",
      "url": "https://example.com",
      "user": {}
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
| `organization` | object |  |
| `path` | string |  |
| `published_timestamp` | date |  |
| `tag_list` | array<string> |  |
| `title` | string |  |
| `url` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Dev.to API, this operation is `GET /articles/latest` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-latest-articles.md) for the provider-specific parameters and requirements.

