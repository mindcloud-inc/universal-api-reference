# Create Index From Backup with Pinecone

Creates a Pinecone index from a backup.

## Endpoint

- **Method:** `POST`
- **Path:** `/backups/:backup_id/create-index`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Create Index From Backup](https://docs.pinecone.io/reference/api/2025-10/control-plane/create_index_from_backup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backup_id` | path | `string` | yes | The ID of the backup to create an index from. |
| `name` | body | `string` | yes | The name of the index to create from the backup. |
