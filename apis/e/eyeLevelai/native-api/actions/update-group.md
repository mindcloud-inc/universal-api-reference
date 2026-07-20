# Update Group with EyeLevel.ai

Updates an existing group in EyeLevel.ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `/group/:groupId`
- **Base URL:** `https://api.groundx.ai/api/v1`
- **Official documentation:** [Update Group](https://docs.eyelevel.ai/reference/api-reference/groups/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `number` | yes | The groupId of the group being updated. |
| `newName` | body | `string` | yes | The new name of the group being renamed. |
