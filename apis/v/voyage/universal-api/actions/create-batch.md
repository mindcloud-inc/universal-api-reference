# Voyage: Create Batch

Creates and executes a batch in Voyage.

```
POST https://connect.mindcloud.co/v1/universal/voyage/latest/actions/create-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voyage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voyage/latest/actions/create-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpoint": "0",
  "inputFileId": "string",
  "completionWindow": "12h",
  "requestParams": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voyage/latest/actions/create-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpoint": "0",
    "inputFileId": "string",
    "completionWindow": "12h",
    "requestParams": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endpoint` | list | yes | Voyage endpoint to run for every request in the batch. One of: `0`, `1`, `2`. |
| `inputFileId` | string | yes | ID of the uploaded JSONL input file. |
| `completionWindow` | list | yes | Time window for batch processing. One of: `0`. Default: `12h`. |
| `requestParams` | object | yes | Parameters applied to each request in the batch. |

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

Through the native Voyage API, this operation is `POST /v1/batches` (base URL `https://api.voyageai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-batch.md) for the provider-specific parameters and requirements.

