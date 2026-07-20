# Dev.to: Get Article By Path

Retrieves a published Dev.to article by username and slug path.

```
GET https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-article-by-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-article-by-path?connectionId=$CONNECTION_ID&username=Ava%20Chen&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen",
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-article-by-path?${params}`, {
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
| `username` | string | yes | Article author's username. |
| `slug` | string | yes | Article slug from the DEV path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body_html": "string",
      "body_markdown": "string",
      "description": "string",
      "id": 1,
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
| `body_html` | string |  |
| `body_markdown` | string |  |
| `description` | string |  |
| `id` | number |  |
| `path` | string |  |
| `published_timestamp` | date |  |
| `tag_list` | array<string> |  |
| `title` | string |  |
| `url` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Dev.to API, this operation is `GET /articles/:username/:slug` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article-by-path.md) for the provider-specific parameters and requirements.

