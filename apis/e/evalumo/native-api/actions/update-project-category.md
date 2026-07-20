# Update Project Category with Evalumo

Updates a project category in Evalumo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/project/:projectId`
- **Base URL:** `https://api.evalumo.com`
- **Official documentation:** [Update Project Category](https://evalumo.apidocumentation.com/reference#tag/project/PATCH/project/{projectId})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Evalumo project identifier. |
| `project_category` | body | `string` | yes | New project category value. |
