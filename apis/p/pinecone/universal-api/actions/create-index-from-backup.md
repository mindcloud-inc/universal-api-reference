# Pinecone: Create Index From Backup

Creates a Pinecone index from a backup.

```
POST https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-index-from-backup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-index-from-backup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "backupId": "d77b28af-b2ba-4d99-834b-5ae618fa7259",
  "name": "mc-stage3-restored-index"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-index-from-backup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "backupId": "d77b28af-b2ba-4d99-834b-5ae618fa7259",
    "name": "mc-stage3-restored-index"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `backupId` | string | yes | The ID of the backup to create an index from. Example: `d77b28af-b2ba-4d99-834b-5ae618fa7259`. |
| `name` | string | yes | The name of the index to create from the backup. Example: `mc-stage3-restored-index`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "indexId": "string",
      "restoreJobId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `indexId` | string |  |
| `restoreJobId` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `POST /backups/:backup_id/create-index` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-index-from-backup.md) for the provider-specific parameters and requirements.

