# Set Own Status with Next Cloud OCS

Sets your status in Next Cloud OCS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ocs/v2.php/apps/user_status/api/v1/user_status/status`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Set Own Status](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#set-your-own-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `statusType` | body | `string` | yes | New status: online, away, dnd, invisible, or offline. |
