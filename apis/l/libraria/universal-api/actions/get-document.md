# Libraria: Get Document

Get a document from a library.

```
GET https://connect.mindcloud.co/v1/universal/libraria/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Libraria `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/libraria/latest/actions/get-document?connectionId=$CONNECTION_ID&libraryId=string&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "libraryId": "string",
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/libraria/latest/actions/get-document?${params}`, {
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
| `libraryId` | string | yes | The ID of the library that owns the document. |
| `documentId` | string | yes | The ID of the document to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "scrapeStatus": "string",
      "sourceUrl": "https://example.com",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Document creation timestamp. |
| `id` | string | Libraria document ID. |
| `scrapeStatus` | string | Provider scrape status for the document. |
| `sourceUrl` | string | Source URL returned by Libraria when available. |
| `updatedAt` | string | Document update timestamp. |
| `url` | string | Source URL stored on the document when present. |

## Native endpoint

Through the native Libraria API, this operation is `GET /library/:library_id/document/:document_id` (base URL `https://api.libraria.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

