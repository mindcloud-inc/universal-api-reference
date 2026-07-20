# Agentset: List Documents

Retrieves documents from an Agentset namespace.

```
GET https://connect.mindcloud.co/v1/universal/agentset/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agentset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/list-documents?connectionId=$CONNECTION_ID&namespaceId=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "namespaceId": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentset/latest/actions/list-documents?${params}`, {
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
      "pagination": {
        "hasMore": true,
        "nextCursor": "string",
        "prevCursor": "string"
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
| `data` | array<object> |  |
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
| `pagination` | object |  |
| `pagination.hasMore` | boolean |  |
| `pagination.nextCursor` | string |  |
| `pagination.prevCursor` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Agentset API, this operation is `GET /v1/namespace/:namespaceId/documents` (base URL `https://api.agentset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

