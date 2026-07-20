# Remove Contacts of a specified group with Routee

Removes contacts of a specified group in Routee.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/groups/my/:groupName/contacts`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Remove Contacts of a specified group](https://docs.routee.net/reference/remove-contacts-of-a-specified-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_name` | path | `string` | yes | The name of the group which contains the contacts |
