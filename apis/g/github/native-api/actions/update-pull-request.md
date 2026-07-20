# Update Pull Request with GitHub

Updates a pull request in a GitHub repository.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/repos/:owner/:repo/pulls/:pull_number`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Update Pull Request](https://docs.github.com/en/rest/pulls/pulls#update-a-pull-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `pull_number` | path | `number` | yes | Pull request number. |
| `title` | body | `string` | no | The title of the pull request. |
| `body` | body | `string` | no | The contents of the pull request. |
| `state` | body | `list<string>` | no | The state of the pull request. Accepted values: `0`, `1`. |
| `base` | body | `string` | no | The branch you want the changes pulled into. |
| `maintainer_can_modify` | body | `boolean` | no | Whether maintainers can modify the pull request branch. |
