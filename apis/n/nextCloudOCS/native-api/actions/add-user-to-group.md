# Add User To Group with Next Cloud OCS

Adds a user to a group in Next Cloud OCS.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocs/v1.php/cloud/users/{{userId}}/groups`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Add User To Group](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html#add-user-to-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupid` | body | `string` | yes | Group ID to add the user to. |
| `userId` | path | `string` | yes | Nextcloud user ID. |
