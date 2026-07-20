# List Pull Request Files with GitHub

Lists files in a GitHub pull request.

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
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `pull_number` | path | `number` | yes | The number that identifies the pull request. |
