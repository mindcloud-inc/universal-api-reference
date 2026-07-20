# Agentset: Delete Document

Deletes a document from Agentset.

```
DELETE https://connect.mindcloud.co/v1/universal/agentset/latest/actions/delete-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agentset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/delete-document?connectionId=$CONNECTION_ID&documentId=string&namespaceId=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "namespaceId": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentset/latest/actions/delete-document?${params}`, {
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
| `documentId` | string | yes | The document ID. |
| `namespaceId` | string | yes | The Agentset namespace ID, prefixed with ns_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "completedAt": "string",
        "config": {},
        "createdAt": "string",
        "error": "string",
        "failedAt": "string",
        "id": "string",
        "ingestJobId": "string",
        "name": "Ava Chen",
        "preProcessingAt": "string",
        "processingAt": "string",
        "properties": {},
        "queuedAt": "string",
        "source": {},
        "status": "string",
        "tenantId": "string",
        "totalCharacters": 1,
        "totalChunks": 1,
        "totalPages": 1,
        "totalTokens": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.completedAt` | string |  |
| `data.config` | object |  |
| `data.createdAt` | string |  |
| `data.error` | string |  |
| `data.failedAt` | string |  |
| `data.id` | string |  |
| `data.ingestJobId` | string |  |
| `data.name` | string |  |
| `data.preProcessingAt` | string |  |
| `data.processingAt` | string |  |
| `data.properties` | object |  |
| `data.queuedAt` | string |  |
| `data.source` | object |  |
| `data.status` | string |  |
| `data.tenantId` | string |  |
| `data.totalCharacters` | number |  |
| `data.totalChunks` | number |  |
| `data.totalPages` | number |  |
| `data.totalTokens` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Agentset API, this operation is `DELETE /v1/namespace/:namespaceId/documents/:documentId` (base URL `https://api.agentset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document.md) for the provider-specific parameters and requirements.

