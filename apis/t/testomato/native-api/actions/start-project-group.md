# Start project group with Testomato

Starts a project group of checks in Testomato.

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:ProjectId/start/area/:AreaId`
- **Base URL:** `https://testomato.com/api`
- **Official documentation:** [Start project group](https://help.testomato.com/api/start-project-group)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `AreaId` | path | `string` | yes |
| `ProjectId` | path | `string` | yes |
