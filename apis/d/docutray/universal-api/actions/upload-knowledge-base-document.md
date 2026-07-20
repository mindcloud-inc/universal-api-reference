# Docutray: Upload Knowledge Base Document



```
POST https://connect.mindcloud.co/v1/universal/docutray/latest/actions/upload-knowledge-base-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/upload-knowledge-base-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "documentId": "string",
  "content": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docutray/latest/actions/upload-knowledge-base-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "documentId": "string",
    "content": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique ID of the Knowledge Base |
| `documentId` | string | yes | Unique document ID |
| `content` | object | yes | Document content in JSON format |
| `metadata` | object | no | Additional document metadata |
| `generateEmbedding` | boolean | no | Automatically generate embedding |

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
| `id` | string |  |
| `knowledgeBaseId` | string |  |
| `metadata` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Docutray API, this operation is `POST api/knowledge-bases/:id/documents` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-knowledge-base-document.md) for the provider-specific parameters and requirements.

