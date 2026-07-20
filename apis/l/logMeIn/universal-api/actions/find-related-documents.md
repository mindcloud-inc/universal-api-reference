# LogMeIn: Find Related Documents

Finds related knowledge base documents in LogMeIn.

```
GET https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/find-related-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/find-related-documents?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/find-related-documents?${params}`, {
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
| `documentId` | string | yes | Required document ID. |
| `limit` | number | no | Maximum number of related documents to return. |
| `minScore` | number | no | Minimum relevance score between 0 and 1. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantIds` | string | no | Comma-separated tenant IDs to filter by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "score": 1,
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
| `score` | number |  |
| `title` | string |  |
| `type` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `GET /resolve/knowledge-base/v2/documents/:documentId/related` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-related-documents.md) for the provider-specific parameters and requirements.

