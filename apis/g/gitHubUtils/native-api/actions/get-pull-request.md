# Get Pull Request with GitHub Utils

Retrieves a pull request from a GitHub repository.

## Endpoint

- **Method:** `GET`
- **Path:** `/repos/:owner/:repo/pulls/:pull_number`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Get Pull Request](https://docs.github.com/en/rest/pulls/pulls#get-a-pull-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `pull_number` | path | `number` | yes | Pull request number in the repository. |
