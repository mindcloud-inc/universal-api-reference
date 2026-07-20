# Create Pull Request with GitHub Utils

Creates a pull request on GitHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/repos/:owner/:repo/pulls`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Create Pull Request](https://docs.github.com/en/rest/pulls/pulls#create-a-pull-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Pull request body. |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `repo` | path | `string` | yes | Repository name. |
| `title` | body | `string` | yes | The title of the new pull request. |
| `head` | body | `string` | yes | The branch or commit where changes are implemented. |
| `base` | body | `string` | yes | The branch you want changes pulled into. |
