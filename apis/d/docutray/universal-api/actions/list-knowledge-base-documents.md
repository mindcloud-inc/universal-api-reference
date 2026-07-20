# Docutray: List Knowledge Base Documents



```
GET https://connect.mindcloud.co/v1/universal/docutray/latest/actions/list-knowledge-base-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/list-knowledge-base-documents?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docutray/latest/actions/list-knowledge-base-documents?${params}`, {
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
| `documentId` | string | no | Filter by document ID |
| `id` | string | yes | Unique ID of the Knowledge Base |
| `search` | string | no | Search in documents |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "documentId": "string",
      "id": "string",
      "knowledgeBaseId": "string",
      "metadata": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object |  |
| `createdAt` | date |  |
| `documentId` | string |  |
| `id` | string |  |
| `knowledgeBaseId` | string |  |
| `metadata` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Docutray API, this operation is `GET api/knowledge-bases/:id/documents` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-knowledge-base-documents.md) for the provider-specific parameters and requirements.

