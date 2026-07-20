# Dev.to: List Article Comments

Lists threaded comments for a Dev.to article or podcast episode.

```
GET https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-article-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-article-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/list-article-comments?${params}`, {
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
| `articleId` | string | no | Article identifier to fetch comments for. |
| `podcastEpisodeId` | string | no | Podcast episode identifier to fetch comments for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body_html": "string",
      "children": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "id_code": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body_html` | string |  |
| `children` | array<object> |  |
| `created_at` | date |  |
| `id_code` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Dev.to API, this operation is `GET /comments` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-article-comments.md) for the provider-specific parameters and requirements.

