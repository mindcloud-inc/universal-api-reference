# Update Task with Jostle

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/tasks/task/:id`
- **Base URL:** `https://api-prod.jostle.us`
- **Official documentation:** [Update Task](https://api.jostle.me/reference/patchtask-1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id of the task |
| `patches[0].op` | body | `string` | no | JSON Patch operation: add, remove, or replace |
| `patches[0].path` | body | `string` | no | JSON Pointer path to modify, for example /title |
| `patches[0].value` | body | `string` | no | Value used by the patch operation when required |
