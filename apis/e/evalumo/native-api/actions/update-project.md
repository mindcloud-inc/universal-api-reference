# Update Project with Evalumo

Updates an existing project in Evalumo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/project/:projectId`
- **Base URL:** `https://api.evalumo.com`
- **Official documentation:** [Update Project](https://evalumo.apidocumentation.com/reference#tag/project/PATCH/project/{projectId})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Evalumo project identifier. |
| `project_category` | body | `string` | yes | New project category value, for example Pending or General. |
