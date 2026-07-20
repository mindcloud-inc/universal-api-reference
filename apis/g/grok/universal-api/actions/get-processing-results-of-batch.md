# Grok: Get Processing Results of Batch

Retrieves processing results for a Grok batch.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-processing-results-of-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-processing-results-of-batch?connectionId=$CONNECTION_ID&batchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/get-processing-results-of-batch?${params}`, {
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
| `batchId` | string | yes | Batch identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed": [
        {
          "batchRequestId": "string",
          "errorMessage": "string"
        }
      ],
      "paginationToken": "string",
      "succeeded": [
        {
          "batchRequestId": "string",
          "response": {}
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed` | array<object> | Failed batch request results. |
| `failed[].batchRequestId` | string | Batch request identifier for a failed result. |
| `failed[].errorMessage` | string | Error message for the failed result. |
| `paginationToken` | string | Pagination token for the next page of results. |
| `succeeded` | array<object> | Successful batch request results. |
| `succeeded[].batchRequestId` | string | Batch request identifier for a successful result. |
| `succeeded[].response` | object | Provider response payload for the successful request. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/batches/:batch_id/results` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-processing-results-of-batch.md) for the provider-specific parameters and requirements.

