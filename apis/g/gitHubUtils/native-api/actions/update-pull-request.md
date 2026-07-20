# Update Pull Request with GitHub Utils

Updates an existing pull request on GitHub.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/repos/:owner/:repo/pulls/:pull_number`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Update Pull Request](https://docs.github.com/en/rest/pulls/pulls#update-a-pull-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | New pull request body. |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `state` | body | `string` | no | Pull request state, such as open or closed. |
| `title` | body | `string` | no | New pull request title. |
| `repo` | path | `string` | yes | Repository name. |
| `pull_number` | path | `number` | yes | Pull request number in the repository. |
