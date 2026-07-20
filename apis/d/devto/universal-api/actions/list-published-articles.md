# Dev.to: List Published Articles

Lists published articles in Dev.to.

```
GET https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-published-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-published-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-published-articles?${params}`, {
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
| `state` | string | no | Article feed state: fresh, rising, or all. |
| `tag` | string | no | Return articles that contain this tag. |
| `tags` | string | no | Comma-separated tags; articles matching any tag are returned. |
| `tagsExclude` | string | no | Comma-separated tags to exclude. |
| `username` | string | no | User or organization username to filter articles. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `top` | number | no | Return popular articles from the last N days. |
| `collectionId` | number | no | Collection identifier to filter articles. |

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

Through the native Dev.to API, this operation is `GET /articles` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-published-articles.md) for the provider-specific parameters and requirements.

