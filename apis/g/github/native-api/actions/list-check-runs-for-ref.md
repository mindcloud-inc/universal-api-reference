# List Check Runs for Ref with GitHub

Retrieves the check runs for a commit, branch, or tag in GitHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/commits/:ref/check-runs`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Check Runs for Ref](https://docs.github.com/en/rest/checks/runs#list-check-runs-for-a-git-reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `ref` | path | `string` | yes | A commit SHA, branch name (heads/BRANCH_NAME), or tag name (tags/TAG_NAME). |
| `check_name` | query | `string` | no | Returns check runs with the specified name. |
| `status` | query | `list<string>` | no | Returns check runs with the specified status. Accepted values: `completed`, `in_progress`, `queued`. |
| `filter` | query | `list<string>` | no | Filters check runs by their completed_at timestamp. latest returns the most recent check runs. Accepted values: `all`, `latest`. |
| `app_id` | query | `number` | no | — |
