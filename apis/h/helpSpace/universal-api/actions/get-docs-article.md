# HelpSpace: Get Docs Article

Retrieves a docs article from HelpSpace.

```
GET https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/get-docs-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/get-docs-article?connectionId=$CONNECTION_ID&articleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "articleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/get-docs-article?${params}`, {
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
| `articleId` | string | yes | HelpSpace docs article identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "docsCategoryId": 1,
      "docsSiteId": 1,
      "id": 1,
      "locale": "string",
      "parentId": 1,
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "subtitle": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "urlWithSlug": "https://example.com",
      "visibility": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `createdAt` | date |  |
| `docsCategoryId` | number |  |
| `docsSiteId` | number |  |
| `id` | number |  |
| `locale` | string |  |
| `parentId` | number |  |
| `publishedAt` | date |  |
| `subtitle` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `urlWithSlug` | string |  |
| `visibility` | number |  |

## Native endpoint

Through the native HelpSpace API, this operation is `GET /docs/articles/{id}` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-docs-article.md) for the provider-specific parameters and requirements.

