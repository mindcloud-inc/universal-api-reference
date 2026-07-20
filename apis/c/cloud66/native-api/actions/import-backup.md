# Import Backup with Cloud 66

Imports a backup into a Cloud 66 stack.

## Endpoint

- **Method:** `POST`
- **Path:** `/stacks/:stack_id/backups`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Import Backup](https://developers.cloud66.com/v3/endpoints/backups/#import-backup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID. |
| `group` | body | `number` | yes | Backup group ID to restore into. |
| `db_type` | body | `string` | yes | Comma-separated database types to import. |
| `remote_url` | body | `string` | yes | URL of the external backup file to import. |
