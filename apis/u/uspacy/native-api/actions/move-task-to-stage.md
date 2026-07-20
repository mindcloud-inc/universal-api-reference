# Move Task To Stage with Uspacy

Moves a task to a Uspacy stage.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/v1/stages/:stageId/moveTask`
- **Base URL:** `https://{site}`
- **Official documentation:** [Move Task To Stage](https://uspacy.readme.io/reference/post_tasks-v1-stages-stageid-movetask-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stageId` | path | `string` | yes | The destination stage ID. |
| `id` | body | `number` | yes | The task ID to move. |
