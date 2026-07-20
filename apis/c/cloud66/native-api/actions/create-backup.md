# Create Backup with Cloud 66

Creates a backup for a Cloud 66 stack.

## Endpoint

- **Method:** `POST`
- **Path:** `/stacks/:stack_id/backups`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Create Backup](https://developers.cloud66.com/v3/endpoints/backups/#create-backup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID. |
| `db_type` | query | `string` | no | Comma-separated database types to back up. |
| `frequency` | query | `string` | no | Cron schedule for the backup task. |
| `keep_count` | query | `number` | no | Number of previous backups to keep. |
| `gzip` | query | `boolean` | no | Whether to gzip the backup. |
| `excluded_tables` | query | `string` | no | Tables to exclude from the backup. |
| `run_on_replica_server` | query | `boolean` | no | Run the backup on a replica server when available. |
