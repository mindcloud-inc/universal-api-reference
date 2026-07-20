# Create Pull Request with GitHub

Creates a pull request in a GitHub repository.

## Endpoint

- **Method:** `POST`
- **Path:** `/repos/:owner/:repo/pulls`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Create Pull Request](https://docs.github.com/en/rest/pulls/pulls#create-a-pull-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `title` | body | `string` | no | The title of the new pull request. |
| `head` | body | `string` | yes | The branch where the changes are implemented. |
| `head_repo` | body | `string` | no | The repository where the changes in the pull request were made when required. |
| `base` | body | `string` | yes | The branch you want the changes pulled into. |
| `body` | body | `string` | no | The contents of the pull request. |
| `maintainer_can_modify` | body | `boolean` | no | Whether maintainers can modify the pull request branch. |
| `draft` | body | `boolean` | no | Whether the pull request is a draft. |
| `issue` | body | `number` | no | An existing issue number to convert into a pull request. |
