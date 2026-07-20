# Update Column with BugHerd

Updates an existing column in a BugHerd project.

## Endpoint

- **Method:** `PUT`
- **Path:** `projects/:project_id/columns/:column_id.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Update Column](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The BugHerd project ID. |
| `column_id` | path | `number` | yes | The BugHerd column ID. |
| `column` | body | `object` | no | Column fields to update. |
| `column.name` | body | `string` | no | The new column name. |
