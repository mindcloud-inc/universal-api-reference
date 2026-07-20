# Describe Backup with Pinecone

Retrieves details for a backup from Pinecone.

## Endpoint

- **Method:** `GET`
- **Path:** `/backups/:backup_id`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Describe Backup](https://docs.pinecone.io/reference/api/2025-10/control-plane/describe_backup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backup_id` | path | `string` | yes | The ID of the backup to describe. |
