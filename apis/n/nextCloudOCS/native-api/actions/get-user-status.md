# Get User Status with Next Cloud OCS

Retrieves user status from Next Cloud OCS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ocs/v2.php/apps/user_status/api/v1/statuses/{{userId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Get User Status](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#fetch-a-specific-users-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Nextcloud user ID. |
