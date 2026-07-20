# Document AI: Get Document Batch Job Status

Retrieves the status and result of a Document AI batch job.

```
GET https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/get-document-batch-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/get-document-batch-job-status?connectionId=$CONNECTION_ID&AsyncJobID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "AsyncJobID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/get-document-batch-job-status?${params}`, {
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
| `AsyncJobID` | string | yes | Cloudmersive async batch job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asyncJobID": "string",
      "asyncJobStatus": "string",
      "errorMessage": "string",
      "extractClassificationResult": {},
      "extractFieldsAndTablesResult": {},
      "extractFieldsResult": {},
      "extractTextResult": {},
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asyncJobID` | string | Cloudmersive asynchronous job ID. |
| `asyncJobStatus` | string | Current async job status. |
| `errorMessage` | string | Provider error message when available. |
| `extractClassificationResult` | object | Completed classification result when available. |
| `extractFieldsAndTablesResult` | object | Completed fields and tables result when available. |
| `extractFieldsResult` | object | Completed field extraction result when available. |
| `extractTextResult` | object | Completed text extraction result when available. |
| `successful` | boolean | Whether the job status request succeeded. |

## Native endpoint

Through the native Document AI API, this operation is `GET /document-ai/document/batch-job/batch-job/status` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-batch-job-status.md) for the provider-specific parameters and requirements.

