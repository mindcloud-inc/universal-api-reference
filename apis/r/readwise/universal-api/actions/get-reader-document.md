# Readwise: Get Reader Document

Retrieves a document from Readwise Reader.

```
GET https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-reader-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-reader-document?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-reader-document?${params}`, {
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
| `id` | string | yes | Reader document ID to fetch. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `withHtmlContent` | boolean | no | Whether to include parsed HTML content in the response. |
| `withRawSourceUrl` | boolean | no | Whether to include the raw source URL in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "category": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "htmlContent": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "location": "string",
      "notes": "string",
      "publishedDate": "2026-05-07T12:00:00.000Z",
      "siteName": "Ava Chen",
      "source": "string",
      "sourceUrl": "https://example.com",
      "summary": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "wordCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string | Document author. |
| `category` | string | Document category. |
| `content` | string | HTML content when requested. |
| `createdAt` | date | Created timestamp. |
| `htmlContent` | string | Parsed HTML content when requested. |
| `id` | string | Reader document ID. |
| `imageUrl` | string | Image URL. |
| `location` | string | Current Reader location. |
| `notes` | string | Document notes. |
| `publishedDate` | date | Published date. |
| `siteName` | string | Site name. |
| `source` | string | Document source. |
| `sourceUrl` | string | Original source URL. |
| `summary` | string | Document summary. |
| `tags` | array<string> | Document tags. |
| `title` | string | Document title. |
| `updatedAt` | date | Updated timestamp. |
| `url` | string | Reader URL for the document. |
| `wordCount` | number | Word count. |

## Native endpoint

Through the native Readwise API, this operation is `GET /api/v3/list/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reader-document.md) for the provider-specific parameters and requirements.

