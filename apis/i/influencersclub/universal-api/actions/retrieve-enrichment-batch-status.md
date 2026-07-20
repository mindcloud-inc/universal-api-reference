# Influencers.club: Retrieve Enrichment Batch Status

Retrieves batch enrichment job status from Influencers.club.

```
GET https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/retrieve-enrichment-batch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/retrieve-enrichment-batch-status?connectionId=$CONNECTION_ID&batchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/retrieve-enrichment-batch-status?${params}`, {
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
| `batchId` | string | yes | Batch identifier to check status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batch_id": "string",
      "credits_used": "string",
      "estimated_completion": "string",
      "failed_count": 1,
      "metadata": {},
      "processed_rows": 1,
      "started_at": "string",
      "status": "string",
      "status_message": "string",
      "success_count": 1,
      "total_rows": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batch_id` | string | Batch identifier. |
| `credits_used` | string | Credits consumed so far. |
| `estimated_completion` | string | Estimated completion timestamp. |
| `failed_count` | number | Rows that failed enrichment. |
| `metadata` | object | Additional batch metadata. |
| `processed_rows` | number | Rows already processed. |
| `started_at` | string | Processing start timestamp. |
| `status` | string | Current batch processing status. |
| `status_message` | string | Human-readable status message. |
| `success_count` | number | Rows enriched successfully. |
| `total_rows` | number | Total rows submitted in the batch. |

## Native endpoint

Through the native Influencers.club API, this operation is `GET /public/v1/enrichment/batch/:batch_id/status/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-enrichment-batch-status.md) for the provider-specific parameters and requirements.

