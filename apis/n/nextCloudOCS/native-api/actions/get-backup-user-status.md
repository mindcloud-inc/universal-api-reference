# Get Backup User Status with Next Cloud OCS

Retrieves backup user status from Next Cloud OCS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ocs/v2.php/apps/user_status/api/v1/statuses/_{{userId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Get Backup User Status](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#fetch-a-users-backup-status)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `userId` | path | `string` | yes |
