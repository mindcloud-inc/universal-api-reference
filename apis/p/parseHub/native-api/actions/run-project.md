# Run Project with ParseHub

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_token}/run`
- **Base URL:** `https://www.parsehub.com/api/v2`
- **Official documentation:** [Run Project](https://www.parsehub.com/docs/ref/api/v2/#run-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_token` | path | `string` | yes | The ParseHub token of the project to run. |
| `start_url` | body | `string` | no | Optional URL to override the project's default start site. |
| `start_template` | body | `string` | no | Optional template name to start the run with. |
| `start_value_override` | body | `string` | no | Optional JSON string of starting global-scope values for the run, such as {"query":"San Francisco"}. |
| `send_email` | body | `number` | no | Set to 1 to send an email when the run completes or errors. |
