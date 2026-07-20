# Create Project Task Assignment with Harvest

Creates a task assignment for a project in Harvest.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/projects/:projectId/task_assignments`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Create Project Task Assignment](https://help.getharvest.com/api-v2/projects-api/projects/task-assignments/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `task_id` | body | `number` | yes |
| `is_active` | body | `boolean` | no |
| `billable` | body | `boolean` | no |
| `hourly_rate` | body | `number` | no |
| `budget` | body | `number` | no |
