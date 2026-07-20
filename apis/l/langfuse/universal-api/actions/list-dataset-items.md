# Langfuse: List Dataset Items

Retrieves dataset items from Langfuse.

```
GET https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-dataset-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-dataset-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-dataset-items?${params}`, {
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
| `datasetName` | string | no |  |
| `sourceObservationId` | string | no |  |
| `sourceTraceId` | string | no |  |
| `version` | string | no |  |

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

Through the native Langfuse API, this operation is `GET /dataset-items` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-dataset-items.md) for the provider-specific parameters and requirements.

