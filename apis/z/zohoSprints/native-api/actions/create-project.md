# Create Project with Zoho Sprints

Creates a new project in Zoho Sprints.

## Endpoint

- **Method:** `POST`
- **Path:** `/team/:teamId/projects/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [Create Project](https://sprints.zoho.com/apidoc.html#Createproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `name` | query | `string` | yes |
| `owner` | query | `string` | yes |
| `projgroup` | query | `string` | yes |
| `description` | body | `string` | no |
