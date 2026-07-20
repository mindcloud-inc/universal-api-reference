# Complete Sprint with Zoho Sprints

Completes an existing sprint in Zoho Sprints.

## Endpoint

- **Method:** `POST`
- **Path:** `/team/:teamId/projects/:projectId/sprints/:sprintId/complete/?action=complete`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [Complete Sprint](https://sprints.zoho.com/apidoc.html#Completesprint)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `sprintId` | path | `string` | yes |
