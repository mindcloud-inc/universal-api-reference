# Readwise: List Books

Retrieves books from the Readwise library.

```
GET https://connect.mindcloud.co/v1/universal/readwise/latest/actions/list-books
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/list-books?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/list-books?${params}`, {
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
| `category` | string | no | Return books within a specific category. |
| `source` | string | no | Return books from a specific source. |
| `updatedLt` | string | no | Return books updated before this ISO 8601 datetime. |
| `updatedGt` | string | no | Return books updated after this ISO 8601 datetime. |
| `lastHighlightAtLt` | string | no | Return books last highlighted before this ISO 8601 datetime. |
| `lastHighlightAtGt` | string | no | Return books last highlighted after this ISO 8601 datetime. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "category": "string",
      "coverImageUrl": "https://example.com",
      "documentNote": "string",
      "highlightsUrl": "https://example.com",
      "id": 1,
      "lastHighlightAt": "string",
      "numHighlights": 1,
      "source": "string",
      "sourceUrl": "https://example.com",
      "title": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `category` | string |  |
| `coverImageUrl` | string |  |
| `documentNote` | string |  |
| `highlightsUrl` | string |  |
| `id` | number |  |
| `lastHighlightAt` | string |  |
| `numHighlights` | number |  |
| `source` | string |  |
| `sourceUrl` | string |  |
| `title` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Readwise API, this operation is `GET /api/v2/books/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-books.md) for the provider-specific parameters and requirements.

