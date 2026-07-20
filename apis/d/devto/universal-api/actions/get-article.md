# Dev.to: Get Article

Retrieves a published Dev.to article by ID.

```
GET https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-article?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-article?${params}`, {
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
| `id` | number | yes | Numeric article ID. |

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

Through the native Dev.to API, this operation is `GET /articles/:id` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article.md) for the provider-specific parameters and requirements.

