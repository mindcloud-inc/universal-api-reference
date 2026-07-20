# LogMeIn: List Documents

Retrieves knowledge base documents from LogMeIn.

```
GET https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/list-documents?${params}`, {
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
| `page` | number | no | Page number starting from 1. |
| `pageSize` | number | no | Number of documents per page. |
| `searchText` | string | no | Search text for document titles, user names, and labels. |
| `sort` | string | no | Sort field, prefix with '-' for descending order. |
| `folderId` | string | no | Folder ID to filter by, or 'none' for documents without a folder. |
| `tenantIds` | string | no | Comma-separated tenant IDs to filter by. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `visibilityFilter` | string | no | Visibility filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "lastModifiedAt": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "type": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `lastModifiedAt` | date |  |
| `title` | string |  |
| `type` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `GET /resolve/knowledge-base/v2/documents` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

