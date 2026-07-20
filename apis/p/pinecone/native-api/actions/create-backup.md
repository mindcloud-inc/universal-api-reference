# Create Backup with Pinecone

Creates a backup for a Pinecone index.

## Endpoint

- **Method:** `POST`
- **Path:** `/indexes/:index_name/backups`
- **Base URL:** `https://api.pinecone.io`
- **Official documentation:** [Create Backup](https://docs.pinecone.io/reference/api/2025-10/control-plane/create_backup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | An optional name for the backup. |
| `description` | body | `string` | no | An optional description for the backup. |
