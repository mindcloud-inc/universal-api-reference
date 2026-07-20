# DocRaptor: List Documents

Retrieves paginated document records from DocRaptor.

```
GET https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocRaptor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/list-documents?${params}`, {
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
      "async": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_at_v2": "2026-05-07T12:00:00.000Z",
      "document_type": "string",
      "domain_id": 1,
      "id": 1,
      "ip_address": "string",
      "javascript": true,
      "name": "Ava Chen",
      "tag": "string",
      "test": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "updated_at_v2": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `async` | boolean | Whether the document was created asynchronously. |
| `created_at` | date | Document creation timestamp. |
| `created_at_v2` | date | Alternate creation timestamp when present. |
| `document_type` | string | Generated document type, such as pdf or xlsx. |
| `domain_id` | number | Associated DocRaptor domain ID when present. |
| `id` | number | DocRaptor document log ID. |
| `ip_address` | string | IP address observed for the document request. |
| `javascript` | boolean | Whether JavaScript rendering was enabled. |
| `name` | string | Document name. |
| `tag` | string | Optional document tag. |
| `test` | boolean | Whether the document was generated in test mode. |
| `updated_at` | date | Document update timestamp. |
| `updated_at_v2` | date | Alternate update timestamp when present. |
| `user_id` | number | DocRaptor user ID that owns the document. |

## Native endpoint

Through the native DocRaptor API, this operation is `GET /docs.json` (base URL `https://api.docraptor.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

