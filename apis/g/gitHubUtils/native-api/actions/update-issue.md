# Update Issue with GitHub Utils

Updates an existing issue on GitHub.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/repos/:owner/:repo/issues/:issue_number`
- **Base URL:** `https://api.github.com`
- **Official documentation:** [Update Issue](https://docs.github.com/en/rest/issues/issues#update-an-issue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | New issue body. |
| `owner` | path | `string` | yes | Repository owner or organization login. |
| `state` | body | `string` | no | Issue state, such as open or closed. |
| `title` | body | `string` | no | New issue title. |
| `repo` | path | `string` | yes | Repository name. |
| `issue_number` | path | `number` | yes | Issue number in the repository. |
