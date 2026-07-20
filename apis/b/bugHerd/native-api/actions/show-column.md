# Show Column with BugHerd

Retrieves a column from a BugHerd project.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_id/columns/:column_id.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Show Column](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The BugHerd project ID. |
| `column_id` | path | `number` | yes | The BugHerd column ID. |
