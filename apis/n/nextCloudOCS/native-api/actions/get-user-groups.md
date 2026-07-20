# Get User Groups with Next Cloud OCS

Retrieves user groups from Next Cloud OCS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ocs/v1.php/cloud/users/{{userId}}/groups`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Get User Groups](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html#get-users-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Nextcloud user ID. |
