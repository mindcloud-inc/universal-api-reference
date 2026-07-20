# Update Project with Kite Suite

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/project/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Project](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | no | — |
| `projectName` | body | `string` | yes | — |
| `projectType` | body | `string` | yes | — |
| `projectLead` | body | `string` | yes | — |
| `avatar` | body | `string` | yes | — |
| `favorite` | body | `boolean` | yes | — |
| `description` | body | `string` | yes | — |
