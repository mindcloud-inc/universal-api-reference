# Remove member from project. with Kite Suite

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/project/member/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Remove member from project.](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | Member ID |
| `projectID` | body | `string` | yes | — |
