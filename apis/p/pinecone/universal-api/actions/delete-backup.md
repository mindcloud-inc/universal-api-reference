# Pinecone: Delete Backup

Deletes a backup from Pinecone.

```
DELETE https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/delete-backup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/delete-backup?connectionId=$CONNECTION_ID&backupId=bbe4c309-c63e-4770-8550-b18ee77b87bd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "backupId": "bbe4c309-c63e-4770-8550-b18ee77b87bd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/delete-backup?${params}`, {
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
| `backupId` | string | yes | The ID of the backup to delete. Example: `bbe4c309-c63e-4770-8550-b18ee77b87bd`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinecone API returns.

## Native endpoint

Through the native Pinecone API, this operation is `DELETE /backups/:backup_id` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-backup.md) for the provider-specific parameters and requirements.

