# Project results with Testomato

Retrieves project check results from Testomato.

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:ProjectId/job/:JobId/results`
- **Base URL:** `https://testomato.com/api`
- **Official documentation:** [Project results](https://help.testomato.com/api/project-results)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `JobId` | path | `string` | yes |
| `ProjectId` | path | `string` | yes |
