# Delete Deal with folk

Deletes an existing deal from folk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/groups/:groupId/:objectType/:objectId`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Delete Deal](https://developer.folk.app/api-reference/deals/delete-a-deal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The group ID that owns the deal object field. |
| `objectType` | path | `string` | yes | The exact deal object type name from group custom fields, such as Deals. |
| `objectId` | path | `string` | yes | The ID of the deal object to delete. |
