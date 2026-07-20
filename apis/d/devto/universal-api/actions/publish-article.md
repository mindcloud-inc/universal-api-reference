# Dev.to: Publish Article

Publishes a new article in Dev.to.

```
POST https://connect.mindcloud.co/v1/universal/devto/latest/actions/publish-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/devto/latest/actions/publish-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/devto/latest/actions/publish-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `article.bodyMarkdown` | string | no | Article body in Markdown. |
| `article.canonicalUrl` | string | no | Optional canonical URL. |
| `article.description` | string | no | Article description or excerpt. |
| `article.mainImage` | string | no | Optional main image URL. |
| `article.series` | string | no | Optional series name. |
| `article.tags` | string | no | Comma-separated article tags. |
| `article.title` | string | no | Article title. |
| `article.published` | boolean | no | Whether to publish immediately. Defaults to false in DEV. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `article.organizationId` | number | no | Optional organization ID to publish under. |

## Response

```json
{
  "success": true,
  "data": [
    {
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

Through the native Dev.to API, this operation is `POST /articles` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-article.md) for the provider-specific parameters and requirements.

