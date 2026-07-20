# Update Project with Zoho Sprints

Updates an existing project in Zoho Sprints.

## Endpoint

- **Method:** `POST`
- **Path:** `/team/:teamId/projects/:projectId/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [Update Project](https://sprints.zoho.com/apidoc.html#Updateproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `name` | query | `string` | no |
| `status` | query | `string` | no |
| `projgroup` | query | `string` | no |
| `owner` | query | `string` | no |
| `startdate` | query | `string` | no |
| `enddate` | query | `string` | no |
| `projectlayoutid` | query | `string` | no |
