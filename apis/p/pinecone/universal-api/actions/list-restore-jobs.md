# Pinecone: List Restore Jobs

Retrieves restore jobs for Pinecone backups.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-restore-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-restore-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-restore-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
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
      "pagination": {
        "next": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].backup_id` | string |  |
| `data[].completed_at` | date |  |
| `data[].created_at` | date |  |
| `data[].percent_complete` | number |  |
| `data[].restore_job_id` | string |  |
| `data[].status` | string |  |
| `data[].target_index_id` | string |  |
| `data[].target_index_name` | string |  |
| `pagination.next` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `GET /restore-jobs` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-restore-jobs.md) for the provider-specific parameters and requirements.

