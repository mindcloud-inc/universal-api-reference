# Xodo Sign: Get Bulk Job Status

Retrieves bulk job status from Xodo Sign.

```
GET https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/get-bulk-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/get-bulk-job-status?connectionId=$CONNECTION_ID&bulkSendingJobId=1&business_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bulkSendingJobId": "1",
  "business_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/get-bulk-job-status?${params}`, {
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
| `bulkSendingJobId` | number | yes | The bulk sending job ID to retrieve. |
| `business_id` | string | yes | The Xodo Sign business ID that owns the bulk job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bulk_job_created_at": "2026-05-07T12:00:00.000Z",
      "bulk_job_owner": {},
      "cancelled_documents": 1,
      "completed_documents": 1,
      "document_count": 1,
      "in_progress_documents": 1,
      "origin_template": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulk_job_created_at` | date | Creation timestamp of the bulk job in UTC. |
| `bulk_job_owner` | object | Owner metadata for the bulk job. |
| `cancelled_documents` | number | Number of cancelled documents in the bulk job. |
| `completed_documents` | number | Number of completed documents in the bulk job. |
| `document_count` | number | Number of documents successfully created by the bulk job. |
| `in_progress_documents` | number | Number of in-progress documents in the bulk job. |
| `origin_template` | object | Template metadata associated with the bulk job. |

## Native endpoint

Through the native Xodo Sign API, this operation is `GET /bulk_job/:bulkSendingJobId/status` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-job-status.md) for the provider-specific parameters and requirements.

