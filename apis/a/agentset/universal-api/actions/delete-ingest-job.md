# Agentset: Delete Ingest Job

Deletes an ingest job from Agentset.

```
DELETE https://connect.mindcloud.co/v1/universal/agentset/latest/actions/delete-ingest-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agentset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/delete-ingest-job?connectionId=$CONNECTION_ID&jobId=string&namespaceId=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "namespaceId": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentset/latest/actions/delete-ingest-job?${params}`, {
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
| `jobId` | string | yes | The ingest job ID. |
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

Through the native Agentset API, this operation is `DELETE /v1/namespace/:namespaceId/ingest-jobs/:jobId` (base URL `https://api.agentset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-ingest-job.md) for the provider-specific parameters and requirements.

