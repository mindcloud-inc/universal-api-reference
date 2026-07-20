# Doctly: List Documents



```
GET https://connect.mindcloud.co/v1/universal/doctly/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doctly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doctly/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doctly/latest/actions/list-documents?${params}`, {
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
| `noExtractor` | boolean | no | Return only plain Markdown conversions without an extractor. Default: `false`. |
| `search` | string | no | Case-insensitive partial filename search. Example: `dummy`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extractorId` | string | no | Filter by a specific extractor UUID. Example: `987fcdeb-a654-3210-9876-543210987654`. |
| `dateFrom` | string | no | Filter documents created on or after this ISO 8601 date. Example: `2026-04-01T00:00:00Z`. |
| `dateTo` | string | no | Filter documents created on or before this ISO 8601 date. Example: `2026-04-30T23:59:59Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accuracy": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "extractorId": "string",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "id": "string",
      "pageCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accuracy` | string |  |
| `createdAt` | date |  |
| `extractorId` | string |  |
| `fileName` | string |  |
| `fileSize` | number |  |
| `id` | string |  |
| `pageCount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Doctly API, this operation is `GET /documents` (base URL `https://api.doctly.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

