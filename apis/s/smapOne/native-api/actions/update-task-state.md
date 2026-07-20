# Update task state with smapOne

Updates an existing task state in smapOne.

## Endpoint

- **Method:** `PUT`
- **Path:** `/preview/Smaps/{smapId}/Versions/{version}/Tasks/{taskId}/State`
- **Base URL:** `https://platform.smapone.com/Backend`
- **Official documentation:** [Update task state](https://platform.smapone.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `list` | yes | Task state operation. Allowed values are Assign or Remove. Accepted values: `0`, `1`. |
| `smapId` | path | `string` | yes | The smap id. |
| `taskId` | path | `string` | yes | The task record id. |
| `userEmail` | body | `string` | no | User email for task assignment. |
| `version` | path | `string` | yes | The smap version in major.minor format. |
