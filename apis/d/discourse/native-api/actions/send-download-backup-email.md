# Send Download Backup Email with Discourse

Sends a Discourse backup download email.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/backups/:filename`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Send Download Backup Email](https://docs.discourse.org/#tag/Backups/operation/sendDownloadBackupEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | path | `string` | yes | Backup filename. |
