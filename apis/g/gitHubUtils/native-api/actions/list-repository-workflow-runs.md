# List Repository Workflow Runs with GitHub Utils

Retrieves workflow runs from a GitHub repository.

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
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
