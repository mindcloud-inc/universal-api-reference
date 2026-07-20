# Readwise: Get Book

Retrieves a book from the Readwise library.

```
GET https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-book
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-book?connectionId=$CONNECTION_ID&bookId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-book?${params}`, {
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
| `bookId` | number | yes | ID of the book to retrieve. |

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

Through the native Readwise API, this operation is `GET /api/v2/books/:book_id/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-book.md) for the provider-specific parameters and requirements.

