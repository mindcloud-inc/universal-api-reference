# Get Process Instance Task Completed By User for Process Template Task with Process Plan

## Endpoint

- **Method:** `GET`
- **Path:** `/process_template_task/:processTemplateTaskId/completed_by_user/:completedByUserId/process_instance_task`
- **Base URL:** `https://apius0.processplan.com/api/v4`
- **Official documentation:** [Get Process Instance Task Completed By User for Process Template Task](https://answers.processplan.com/c/api/api-endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `completedByUserId` | path | `string` | no | Completed by user ID. |
| `processTemplateTaskId` | path | `string` | no | Process template task ID. |
