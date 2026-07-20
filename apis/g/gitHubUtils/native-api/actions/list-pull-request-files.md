# List Pull Request Files with GitHub Utils

Retrieves files from a GitHub pull request.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/pulls/:pull_number/files`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Pull Request Files](https://docs.github.com/en/rest/pulls/pulls#list-pull-requests-files)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `pull_number` | path | `number` | yes | Pull request number in the repository. |
