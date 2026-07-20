# Pinecone: Create Backup

Creates a backup for a Pinecone index.

```
POST https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-backup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-backup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-backup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | An optional name for the backup. Example: `mc-stage3-backup`. |
| `description` | string | no | An optional description for the backup. Example: `Stage 3 backup smoke test`. |

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

Through the native Pinecone API, this operation is `POST /indexes/:index_name/backups` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-backup.md) for the provider-specific parameters and requirements.

