# Readwise: List Reader Documents

Retrieves documents from the Readwise Reader library.

```
GET https://connect.mindcloud.co/v1/universal/readwise/latest/actions/list-reader-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/list-reader-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/list-reader-documents?${params}`, {
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
| `updatedAfter` | string | no | Fetch only documents updated after this ISO 8601 datetime. |
| `category` | string | no | Filter documents by category. |
| `limit` | number | no | Maximum number of documents to return. |
| `pageCursor` | string | no | Cursor returned by a previous request to continue fetching documents. |
| `withHtmlContent` | boolean | no | Include html_content in each document. |
| `withRawSourceUrl` | boolean | no | Include raw_source_url in each document when available. |
| `location` | string | no | Reader document location: new, later, shortlist, archive, or feed. |
| `tag` | string | no | Reader tag key. Pass an empty value to find untagged documents. Accepts multiple values in one string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "category": "string",
      "createdAt": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "location": "string",
      "notes": "string",
      "siteName": "Ava Chen",
      "sourceUrl": "https://example.com",
      "summary": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updatedAt": "string",
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
| `author` | string |  |
| `category` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `location` | string |  |
| `notes` | string |  |
| `siteName` | string |  |
| `sourceUrl` | string |  |
| `summary` | string |  |
| `tags[]` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `wordCount` | number |  |

## Native endpoint

Through the native Readwise API, this operation is `GET /api/v3/list/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reader-documents.md) for the provider-specific parameters and requirements.

