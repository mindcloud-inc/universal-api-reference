# List Pull Request Reviews with GitHub

Retrieves the reviews submitted on a GitHub pull request.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/pulls/:pull_number/reviews`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [List Pull Request Reviews](https://docs.github.com/en/rest/pulls/reviews#list-reviews-for-a-pull-request)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | The account owner of the repository. The name is not case sensitive. |
| `repo` | path | `string` | yes | The name of the repository without the .git extension. The name is not case sensitive. |
| `pull_number` | path | `number` | yes | The number that identifies the pull request. |
