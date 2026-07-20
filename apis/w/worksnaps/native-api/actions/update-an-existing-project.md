# Update an existing project with Worksnaps

Updates an existing project in Worksnaps.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/{project_id}.xml`
- **Base URL:** `https://api.worksnaps.com/api`
- **Official documentation:** [Update an existing project](https://api.worksnaps.com/api_docs/worksnaps.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | ID of the target project that need to be updated |
| `body` | body | `string` | yes | Raw XML request body for this Worksnaps endpoint. |
