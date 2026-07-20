# GitBook: Get Space Page

Retrieves a page from a GitBook space.

```
GET https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/get-space-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/get-space-page?connectionId=$CONNECTION_ID&pageId=string&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string",
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/get-space-page?${params}`, {
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
| `format` | string | no |  |
| `metadata` | boolean | no |  |
| `pageId` | string | yes |  |
| `spaceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "document": {
        "data": {
          "schemaVersion": 1
        },
        "nodes": [
          {}
        ],
        "object": "string"
      },
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
| `document.data.schemaVersion` | number |  |
| `document.nodes` | array<object> |  |
| `document.object` | string |  |
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

Through the native GitBook API, this operation is `GET /spaces/:spaceId/content/page/:pageId` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-space-page.md) for the provider-specific parameters and requirements.

