# Delete Task with iLovePDFv2

Deletes an iLovePDFv2 task and its files.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://:server/v1/task/:task`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Delete Task](https://www.iloveapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server` | path | `string` | yes | Processing server from Start Task. |
| `task` | path | `string` | yes | Task ID to delete. |
