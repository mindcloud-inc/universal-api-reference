# Get Workflow Run with GitHub

Retrieves a workflow run from GitHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/actions/runs/:run_id`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Get Workflow Run](https://docs.github.com/en/rest/actions/workflow-runs#get-a-workflow-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `run_id` | path | `number` | yes | The unique identifier of the workflow run. |
| `exclude_pull_requests` | query | `boolean` | no | If true, omit pull requests from the response. |
