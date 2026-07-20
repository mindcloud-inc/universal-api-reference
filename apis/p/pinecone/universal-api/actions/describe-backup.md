# Pinecone: Describe Backup

Retrieves details for a backup from Pinecone.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-backup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-backup?connectionId=$CONNECTION_ID&backupId=bbe4c309-c63e-4770-8550-b18ee77b87bd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "backupId": "bbe4c309-c63e-4770-8550-b18ee77b87bd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-backup?${params}`, {
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
| `backupId` | string | yes | The ID of the backup to describe. Example: `bbe4c309-c63e-4770-8550-b18ee77b87bd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backup_id": "string",
      "cloud": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "dimension": 1,
      "name": "Ava Chen",
      "namespace_count": 1,
      "record_count": 1,
      "region": "string",
      "size_bytes": 1,
      "source_index_id": "string",
      "source_index_name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backup_id` | string |  |
| `cloud` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `dimension` | number |  |
| `name` | string |  |
| `namespace_count` | number |  |
| `record_count` | number |  |
| `region` | string |  |
| `size_bytes` | number |  |
| `source_index_id` | string |  |
| `source_index_name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `GET /backups/:backup_id` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-backup.md) for the provider-specific parameters and requirements.

