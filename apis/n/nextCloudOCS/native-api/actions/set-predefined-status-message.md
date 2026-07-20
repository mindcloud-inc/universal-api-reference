# Set Predefined Status Message with Next Cloud OCS

Sets a predefined status message in Next Cloud OCS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ocs/v2.php/apps/user_status/api/v1/user_status/message/predefined`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Set Predefined Status Message](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-status-api.html#set-a-custom-message-predefined)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `clearAt` | body | `number` | no |
| `messageId` | body | `string` | yes |
