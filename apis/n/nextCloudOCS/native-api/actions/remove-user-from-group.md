# Remove User From Group with Next Cloud OCS

Removes a user from a group in Next Cloud OCS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/ocs/v1.php/cloud/users/{{userId}}/groups`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Remove User From Group](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html#remove-user-from-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupid` | body | `string` | yes | Group ID to remove the user from. |
| `userId` | path | `string` | yes | Nextcloud user ID. |
