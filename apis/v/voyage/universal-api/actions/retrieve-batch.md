# Voyage: Retrieve Batch

Retrieves a batch from Voyage.

```
GET https://connect.mindcloud.co/v1/universal/voyage/latest/actions/retrieve-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voyage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voyage/latest/actions/retrieve-batch?connectionId=$CONNECTION_ID&batchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voyage/latest/actions/retrieve-batch?${params}`, {
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
| `batchId` | string | yes | ID of the batch to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelledAt": "string",
      "cancellingAt": "string",
      "completedAt": "string",
      "completionWindow": "string",
      "createdAt": "string",
      "endpoint": "string",
      "errorFileId": "string",
      "errors": {},
      "expectedCompletionAt": "string",
      "failedAt": "string",
      "finalizingAt": "string",
      "id": "string",
      "inProgressAt": "string",
      "inputFileId": "string",
      "metadata": {},
      "model": "string",
      "object": "string",
      "outputFileId": "string",
      "requestCounts": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelledAt` | string | Timestamp when cancellation completed. |
| `cancellingAt` | string | Timestamp when cancellation started. |
| `completedAt` | string | Timestamp when processing completed. |
| `completionWindow` | string | Requested batch completion window. |
| `createdAt` | string | Batch creation timestamp. |
| `endpoint` | string | Target endpoint executed by the batch. |
| `errorFileId` | string | Error file ID when available. |
| `errors` | object | Batch-level error information when present. |
| `expectedCompletionAt` | string | Expected completion timestamp. |
| `failedAt` | string | Timestamp when processing failed. |
| `finalizingAt` | string | Timestamp when finalization started. |
| `id` | string | Voyage batch ID. |
| `inProgressAt` | string | Timestamp when processing started. |
| `inputFileId` | string | Input file ID used by the batch. |
| `metadata` | object | User-supplied metadata when present. |
| `model` | string | Model used for batch requests when present. |
| `object` | string | Object type for the batch. |
| `outputFileId` | string | Output file ID when available. |
| `requestCounts` | object | Request count summary for the batch. |
| `status` | string | Current batch status. |

## Native endpoint

Through the native Voyage API, this operation is `GET /v1/batches/:batchId` (base URL `https://api.voyageai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-batch.md) for the provider-specific parameters and requirements.

