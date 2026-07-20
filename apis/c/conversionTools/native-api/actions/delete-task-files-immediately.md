# Delete Task Files Immediately with Conversion Tools

Permanently deletes a task's files from Conversion Tools.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/delete`
- **Base URL:** `https://api.conversiontools.io/v1`
- **Official documentation:** [Delete Task Files Immediately](https://api.conversiontools.io/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The task ID whose files should be deleted. |
