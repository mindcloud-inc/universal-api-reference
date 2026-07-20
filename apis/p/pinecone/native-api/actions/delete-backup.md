# Delete Backup with Pinecone

Deletes a backup from Pinecone.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/backups/:backup_id`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Delete Backup](https://docs.pinecone.io/reference/api/2025-10/control-plane/delete_backup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backup_id` | path | `string` | yes | The ID of the backup to delete. |
