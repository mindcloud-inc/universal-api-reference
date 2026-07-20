# Get Group Members with Next Cloud OCS

Retrieves group members from Next Cloud OCS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ocs/v1.php/cloud/groups/{{groupId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Get Group Members](https://docs.nextcloud.com/server/latest/admin_manual/configuration_user/instruction_set_for_groups.html#get-members-of-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Nextcloud group ID. |
