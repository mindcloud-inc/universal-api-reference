# Get Sprint Details with Zoho Sprints

Retrieves sprint details from Zoho Sprints.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/projects/:projectId/sprints/:sprintId/?action=details`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [Get Sprint Details](https://sprints.zoho.com/apidoc.html#Getsprintdetails)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `sprintId` | path | `string` | yes |
