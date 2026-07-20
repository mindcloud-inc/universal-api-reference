# Create Backup with Discourse

Creates a new backup in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/backups.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Create Backup](https://docs.discourse.org/#tag/Backups/operation/createBackup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `with_uploads` | body | `boolean` | yes | Whether to include uploads in the backup. |
