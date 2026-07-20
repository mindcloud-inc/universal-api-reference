# Create Column with BugHerd

Creates a new column in a BugHerd project.

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:project_id/columns.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Create Column](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `column` | body | `object` | no |
| `column.name` | body | `string` | yes |
