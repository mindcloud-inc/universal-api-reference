# Remove Tag for Process Instance Task with Process Plan

## Endpoint

- **Method:** `POST`
- **Path:** `/process_instance_task/:processInstanceTaskId/tag/:tagId/remove`
- **Base URL:** `https://apius0.processplan.com/api/v4`
- **Official documentation:** [Remove Tag for Process Instance Task](https://answers.processplan.com/c/api/api-endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processInstanceTaskId` | path | `string` | no | Process instance task ID. |
| `tagId` | path | `string` | no | Tag ID. |
