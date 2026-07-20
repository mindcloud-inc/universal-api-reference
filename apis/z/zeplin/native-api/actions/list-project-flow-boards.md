# List Project Flow Boards with Zeplin

Retrieves a list of project flow boards from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/flow_boards`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Flow Boards](https://docs.zeplin.dev/reference/getprojectflowboards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
