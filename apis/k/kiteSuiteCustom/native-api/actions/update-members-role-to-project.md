# Update member's role to project. with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/project/member/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update member's role to project.](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | Member ID |
| `projectID` | body | `string` | yes | — |
| `roleID` | body | `string` | yes | — |
