# List Tags with Zoho Sprints

Retrieves tags from Zoho Sprints.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/tags/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [List Tags](https://sprints.zoho.com/apidoc.html#Gettags)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `index` | query | `number` | yes |
| `range` | query | `number` | yes |
| `tagIdarr[]` | query | `array<string>` | no |
| `searchvalue` | query | `string` | no |
