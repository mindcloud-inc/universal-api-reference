# List Repository Workflow Runs with GitHub

Lists workflow runs in a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/actions/runs`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Repository Workflow Runs](https://docs.github.com/en/rest/actions/workflow-runs#list-workflow-runs-for-a-repository)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `actor` | query | `string` | no | Return workflow runs for the specified actor login. |
| `branch` | query | `string` | no | Return workflow runs associated with a branch name. |
| `event` | query | `string` | no | Return workflow runs triggered by the specified event. |
| `status` | query | `string` | no | Return workflow runs with the specified status or conclusion. |
| `created` | query | `string` | no | Return workflow runs created within the specified date-time range syntax. |
| `exclude_pull_requests` | query | `boolean` | no | If true, omit pull requests from the response. |
| `check_suite_id` | query | `number` | no | Return workflow runs with the specified check suite ID. |
| `head_sha` | query | `string` | no | Only return workflow runs associated with the specified head SHA. |
