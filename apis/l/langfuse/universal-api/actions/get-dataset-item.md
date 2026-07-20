# Langfuse: Get Dataset Item

Retrieves a dataset item from Langfuse.

```
GET https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-dataset-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-dataset-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-dataset-item?${params}`, {
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
| `id` | string | no |  |

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

Through the native Langfuse API, this operation is `GET /dataset-items/:id` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dataset-item.md) for the provider-specific parameters and requirements.

