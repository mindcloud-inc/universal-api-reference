# Update User Field with Next Cloud OCS

Updates a user field in Next Cloud OCS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ocs/v1.php/cloud/users/{{userId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Update User Field](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_users.html#edit-data-of-a-single-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Editable user field key, such as email, displayname, phone, address, website, twitter, password, or quota. |
| `userId` | path | `string` | yes | Nextcloud user ID. |
| `value` | body | `string` | yes | New value for the selected field. |
