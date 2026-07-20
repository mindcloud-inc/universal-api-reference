# Delete Task with iLoveSign

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://:server/v1/task/:task`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Delete Task](https://www.iloveapi.com/docs/api-reference#task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server` | path | `string` | yes | Task-assigned host returned by the start call. |
| `task` | path | `string` | yes | Task identifier to delete. |
