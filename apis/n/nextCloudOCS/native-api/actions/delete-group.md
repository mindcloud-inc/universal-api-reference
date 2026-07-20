# Delete Group with Next Cloud OCS

Deletes a group from Next Cloud OCS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/ocs/v1.php/cloud/groups/{{groupId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Delete Group](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html#delete-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Nextcloud group ID. |
