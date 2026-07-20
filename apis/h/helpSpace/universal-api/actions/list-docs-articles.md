# HelpSpace: List Docs Articles

Retrieves docs articles from HelpSpace.

```
GET https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-docs-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-docs-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/list-docs-articles?${params}`, {
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

Through the native HelpSpace API, this operation is `GET /docs/articles` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-docs-articles.md) for the provider-specific parameters and requirements.

