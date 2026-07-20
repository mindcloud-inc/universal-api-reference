# Agentset: Create Ingest Job

Creates an ingest job in an Agentset namespace.

```
POST https://connect.mindcloud.co/v1/universal/agentset/latest/actions/create-ingest-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agentset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/create-ingest-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "namespaceId": "Ava Chen",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentset/latest/actions/create-ingest-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "namespaceId": "Ava Chen",
    "payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `namespaceId` | string | yes | The Agentset namespace ID, prefixed with ns_. |
| `payload` | object | yes | The ingest payload to submit. |

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
        "externalId": "string",
        "failedAt": "string",
        "id": "string",
        "name": "Ava Chen",
        "namespaceId": "Ava Chen",
        "payload": {},
        "preProcessingAt": "string",
        "processingAt": "string",
        "queuedAt": "string",
        "status": "string",
        "tenantId": "string"
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
| `data.externalId` | string |  |
| `data.failedAt` | string |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.namespaceId` | string |  |
| `data.payload` | object |  |
| `data.preProcessingAt` | string |  |
| `data.processingAt` | string |  |
| `data.queuedAt` | string |  |
| `data.status` | string |  |
| `data.tenantId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Agentset API, this operation is `POST /v1/namespace/:namespaceId/ingest-jobs` (base URL `https://api.agentset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ingest-job.md) for the provider-specific parameters and requirements.

