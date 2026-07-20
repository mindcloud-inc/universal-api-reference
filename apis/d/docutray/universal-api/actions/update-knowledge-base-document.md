# Docutray: Update Knowledge Base Document



```
PUT https://connect.mindcloud.co/v1/universal/docutray/latest/actions/update-knowledge-base-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/update-knowledge-base-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docutray/latest/actions/update-knowledge-base-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | Unique ID of the document |
| `id` | string | yes | Unique ID of the Knowledge Base |
| `content` | object | no | New document content |
| `metadata` | object | no | Updated metadata |
| `regenerateEmbedding` | boolean | no | Force embedding regeneration |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "documentId": "string",
      "embeddingStatus": "string",
      "hasEmbedding": true,
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
| `embeddingStatus` | string |  |
| `hasEmbedding` | boolean |  |
| `id` | string |  |
| `knowledgeBaseId` | string |  |
| `metadata` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Docutray API, this operation is `PUT api/knowledge-bases/:id/documents/:documentId` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-knowledge-base-document.md) for the provider-specific parameters and requirements.

