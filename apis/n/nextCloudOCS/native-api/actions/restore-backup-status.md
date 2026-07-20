# Restore Backup Status with Next Cloud OCS

Restores a backup status in Next Cloud OCS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/ocs/v2.php/apps/user_status/api/v1/statuses/revert/{{messageId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Restore Backup Status](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#user-status-restore-backup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Backup status message ID. |
