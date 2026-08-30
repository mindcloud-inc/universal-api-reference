# Associate Task with Project with HubSpot

## Endpoint

- **Method:** `PUT`
- **Path:** `crm/objects/2026-03/tasks/:taskId/associations/default/projects/:projectId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Associate Task with Project](https://developers.hubspot.com/docs/api-reference/latest/crm/associations/associate-records/guide)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
