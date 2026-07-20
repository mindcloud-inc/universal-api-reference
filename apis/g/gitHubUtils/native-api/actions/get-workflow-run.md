# Get Workflow Run with GitHub Utils

Retrieves a workflow run from a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/actions/runs/:run_id`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Get Workflow Run](https://docs.github.com/en/rest/actions/workflow-runs#get-a-workflow-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `run_id` | path | `number` | yes | GitHub Actions workflow run ID. |
