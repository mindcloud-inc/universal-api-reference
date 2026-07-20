# Update Deal with folk

Updates an existing deal in folk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/groups/:groupId/:objectType/:objectId`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Update Deal](https://developer.folk.app/api-reference/deals/update-a-deal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The group ID that owns the deal object field. |
| `objectType` | path | `string` | yes | The exact deal object type name from group custom fields, such as Deals. |
| `objectId` | path | `string` | yes | The ID of the deal object to update. |
| `name` | body | `string` | no | The updated display name of the deal. |
