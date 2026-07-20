# Xodo Sign: Get Bulk Job

Retrieves a bulk job from Xodo Sign.

```
GET https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/get-bulk-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xodo Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/get-bulk-job?connectionId=$CONNECTION_ID&bulkSendingJobId=1&business_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bulkSendingJobId": "1",
  "business_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/get-bulk-job?${params}`, {
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
      "business_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "document_count": 1,
      "entry_id": 1,
      "status": "string",
      "template_hash": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `business_id` | number | Business ID that created the bulk job. |
| `created_at` | date | Creation timestamp of the bulk job in UTC. |
| `document_count` | number | Number of documents created by the bulk job. |
| `entry_id` | number | Unique database ID of the bulk job. |
| `status` | string | Current bulk job status. |
| `template_hash` | string | Template hash used for the bulk job. |
| `user_id` | number | User ID that requested the bulk job. |

## Native endpoint

Through the native Xodo Sign API, this operation is `GET /bulk_job/:bulkSendingJobId` (base URL `https://api.eversign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-job.md) for the provider-specific parameters and requirements.

