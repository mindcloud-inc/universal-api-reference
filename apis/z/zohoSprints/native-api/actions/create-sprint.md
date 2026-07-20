# Create Sprint with Zoho Sprints

Creates a new sprint in Zoho Sprints.

## Endpoint

- **Method:** `POST`
- **Path:** `/team/:teamId/projects/:projectId/sprints/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [Create Sprint](https://sprints.zoho.com/apidoc.html#Createsprint)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `name` | query | `string` | yes |
