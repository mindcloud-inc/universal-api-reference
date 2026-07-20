# Pinecone: Describe Restore Job

Retrieves details for a restore job from Pinecone.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-restore-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-restore-job?connectionId=$CONNECTION_ID&jobId=7df5ef34-c22d-4bbc-89fb-2706f450fe53" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "7df5ef34-c22d-4bbc-89fb-2706f450fe53"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-restore-job?${params}`, {
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
| `jobId` | string | yes | The ID of the restore job to describe. Example: `7df5ef34-c22d-4bbc-89fb-2706f450fe53`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backup_id": "string",
      "completed_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "percent_complete": 1,
      "restore_job_id": "string",
      "status": "string",
      "target_index_id": "string",
      "target_index_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backup_id` | string |  |
| `completed_at` | date |  |
| `created_at` | date |  |
| `percent_complete` | number |  |
| `restore_job_id` | string |  |
| `status` | string |  |
| `target_index_id` | string |  |
| `target_index_name` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `GET /restore-jobs/:job_id` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-restore-job.md) for the provider-specific parameters and requirements.

