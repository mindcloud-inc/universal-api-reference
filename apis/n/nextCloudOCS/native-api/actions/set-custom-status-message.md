# Set Custom Status Message with Next Cloud OCS

Sets custom status message in Next Cloud OCS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ocs/v2.php/apps/user_status/api/v1/user_status/message/custom`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Set Custom Status Message](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#set-a-custom-message-user-defined)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Custom status message. |
