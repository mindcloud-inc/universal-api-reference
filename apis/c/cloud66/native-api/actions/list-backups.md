# List Backups with Cloud 66

Retrieves backups from your Cloud 66 account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks/:id/backups`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [List Backups](https://developers.cloud66.com/v3/endpoints/backups/#list-backups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The stack UID |
| `group` | query | `number` | no | Backup group ID |
| `db_type` | query | `string` | no | Backup database type |
