# Create task with smapOne

Creates a new task in smapOne.

## Endpoint

- **Method:** `POST`
- **Path:** `/preview/Smaps/{smapId}/Versions/{version}/Tasks`
- **Base URL:** `https://platform.smapone.com/Backend`
- **Official documentation:** [Create task](https://platform.smapone.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment` | body | `string` | no | Comment from the creator of the task. |
| `data` | body | `object` | no | Task prefill data object matching the smap schema. |
| `hasPriority` | body | `boolean` | no | Whether the task is prioritized. |
| `smapId` | path | `string` | yes | The smap id. |
| `title` | body | `string` | yes | Name of the task or data record. |
| `userEmail` | body | `string` | no | User email to assign the task to. |
| `version` | path | `string` | yes | The smap version in major.minor format. |
