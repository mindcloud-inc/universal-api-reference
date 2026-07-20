# Langfuse: Create Dataset Run Item

Creates a dataset run item in Langfuse.

```
POST https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-dataset-run-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-dataset-run-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-dataset-run-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdAt` | string | no |  |
| `datasetItemId` | string | no |  |
| `datasetVersion` | string | no |  |
| `metadata` | string | no |  |
| `observationId` | string | no |  |
| `runDescription` | string | no |  |
| `runName` | string | no |  |
| `traceId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "datasetItemId": "string",
      "datasetRunId": "string",
      "datasetRunName": "Ava Chen",
      "id": "string",
      "observationId": "string",
      "traceId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `datasetItemId` | string |  |
| `datasetRunId` | string |  |
| `datasetRunName` | string |  |
| `id` | string |  |
| `observationId` | string |  |
| `traceId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Langfuse API, this operation is `POST /dataset-run-items` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset-run-item.md) for the provider-specific parameters and requirements.

