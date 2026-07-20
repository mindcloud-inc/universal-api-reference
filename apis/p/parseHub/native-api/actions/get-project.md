# Get Project with ParseHub

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_token}`
- **Base URL:** `https://www.parsehub.com/api/v2`
- **Official documentation:** [Get Project](https://www.parsehub.com/docs/ref/api/v2/#get-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_token` | path | `string` | yes | The ParseHub token of the project to fetch. |
| `offset` | query | `number` | no | Zero-based offset into the project's run_list. |
| `include_options` | query | `number` | no | Set to 1 to include project options_json in the response. |
