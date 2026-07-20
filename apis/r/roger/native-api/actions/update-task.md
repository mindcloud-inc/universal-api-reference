# Update Task with Roger

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/:id`
- **Base URL:** `https://api.rogerroger.io`
- **Official documentation:** [Update Task](https://developer.rogerroger.io/tasks)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Task identifier. |
| `description` | body | `string` | yes | Updated task description. |
