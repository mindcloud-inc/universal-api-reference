# Start Sprint with Zoho Sprints

Starts an existing sprint in Zoho Sprints.

## Endpoint

- **Method:** `POST`
- **Path:** `/team/:teamId/projects/:projectId/sprints/:sprintId/start/?action=start`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [Start Sprint](https://sprints.zoho.com/apidoc.html#Startsprint)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `sprintId` | path | `string` | yes |
