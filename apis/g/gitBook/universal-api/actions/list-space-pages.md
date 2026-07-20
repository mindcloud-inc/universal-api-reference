# GitBook: List Space Pages

Retrieves pages from a GitBook space.

```
GET https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-space-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-space-pages?connectionId=$CONNECTION_ID&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-space-pages?${params}`, {
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
| `computed` | boolean | no |  |
| `metadata` | boolean | no |  |
| `spaceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "kind": "string",
      "layout": {
        "cover": true,
        "coverSize": "string",
        "description": true,
        "metadata": true,
        "outline": true,
        "pagination": true,
        "tableOfContents": true,
        "tags": true,
        "title": true,
        "width": "string"
      },
      "pages": [
        {}
      ],
      "path": "string",
      "slug": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "type": "string",
      "urls": {
        "app": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `kind` | string |  |
| `layout.cover` | boolean |  |
| `layout.coverSize` | string |  |
| `layout.description` | boolean |  |
| `layout.metadata` | boolean |  |
| `layout.outline` | boolean |  |
| `layout.pagination` | boolean |  |
| `layout.tableOfContents` | boolean |  |
| `layout.tags` | boolean |  |
| `layout.title` | boolean |  |
| `layout.width` | string |  |
| `pages` | array<object> |  |
| `path` | string |  |
| `slug` | string |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `type` | string |  |
| `urls.app` | string |  |

## Native endpoint

Through the native GitBook API, this operation is `GET /spaces/:spaceId/content/pages` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-space-pages.md) for the provider-specific parameters and requirements.

