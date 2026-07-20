# Langfuse: Create Dataset Item

Creates a dataset item in Langfuse.

```
POST https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-dataset-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-dataset-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-dataset-item', {
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
| `datasetName` | string | no |  |
| `expectedOutput` | string | no |  |
| `id` | string | no |  |
| `input` | string | no |  |
| `metadata` | string | no |  |
| `sourceObservationId` | string | no |  |
| `sourceTraceId` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "datasetId": "string",
      "datasetName": "Ava Chen",
      "expectedOutput": "string",
      "id": "string",
      "input": "string",
      "metadata": "string",
      "sourceObservationId": "string",
      "sourceTraceId": "string",
      "status": "string",
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
| `datasetId` | string |  |
| `datasetName` | string |  |
| `expectedOutput` | string |  |
| `id` | string |  |
| `input` | string |  |
| `metadata` | string |  |
| `sourceObservationId` | string |  |
| `sourceTraceId` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Langfuse API, this operation is `POST /dataset-items` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset-item.md) for the provider-specific parameters and requirements.

