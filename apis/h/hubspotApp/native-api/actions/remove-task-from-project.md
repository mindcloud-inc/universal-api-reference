# Remove Task from Project with HubSpot

## Endpoint

- **Method:** `DELETE`
- **Path:** `crm/objects/2026-03/tasks/:taskId/associations/projects/:projectId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Remove Task from Project](https://developers.hubspot.com/docs/api-reference/latest/crm/associations/associate-records/guide)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
